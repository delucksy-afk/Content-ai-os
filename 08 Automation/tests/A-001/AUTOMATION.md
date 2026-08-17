# Automation Test — A-001

**Automation ID:** A-2026-08-17-001  
**Version:** v0.1  
**Status:** TESTED  
**Source Workflow:** W-2026-08-17-001  
**Knowledge:** K-2026-08-17-001  
**Prompt:** P-2026-08-17-001  
**Script:** S-2026-08-17-001  
**Thumbnail:** T-2026-08-17-001

## Goal

ทดสอบการ Orchestrate Content Packaging Pipeline โดยไม่ให้ Automation ข้าม Quality Gates หรือ Human Review

## Trigger

ได้รับ Brief ที่มี Topic, Audience, Promise และ Format ครบ

## Input Validation

```text
IF required fields missing
→ NEEDS_INPUT
→ STOP
```

## Execution

```text
1. Validate Brief
2. Resolve Knowledge Version
3. Resolve Prompt Version
4. Execute W-001
5. Generate / validate Script artifact
6. Generate / validate Thumbnail package
7. Run quality gates
8. WAITING_REVIEW เมื่อจำเป็น
9. Persist approved package
10. Emit handoff + metrics
```

## State Model

```text
QUEUED
  ↓
RUNNING
  ├── NEEDS_INPUT
  ├── RETRYING
  ├── FAILED
  └── WAITING_REVIEW
          ↓
      SUCCEEDED
```

## Retry Policy

Retry เฉพาะ transient failure เช่น temporary dependency failure และต้องมี bounded retry

ไม่ Retry validation failure หรือ policy failure โดยอัตโนมัติ

## Idempotency

ใช้ `Run ID + Item ID + Workflow Version` เป็น logical identity เพื่อป้องกันการสร้าง package ซ้ำโดยไม่ตั้งใจ

## Human Gate

ต้องส่ง Human Review เมื่อ:

- Quality Gate ไม่ผ่าน
- Claim สำคัญยังไม่ verified
- Thumbnail มี misleading risk
- Output มี ambiguity สูง
- มีการเปลี่ยน dependency สำคัญ

## Security

- ไม่เก็บ Credentials ใน Repository
- ใช้ platform secret storage
- ใช้ Least Privilege
- Log เฉพาะข้อมูลที่จำเป็น

## Observability

บันทึก:

- Run ID
- State transitions
- Dependency versions
- Retry count
- Failure category
- Human review result
- Output reference

## Failure Matrix

| Failure | Expected State | Action |
|---|---|---|
| Missing input | NEEDS_INPUT | Stop |
| Temporary tool failure | RETRYING | Bounded retry |
| Validation failure | FAILED / REWORK | Human / Workflow rework |
| Policy risk | WAITING_REVIEW | Human decision |
| Duplicate run | Existing / controlled re-run | Do not duplicate output |

## Output Contract

```text
Content Package
├── Run ID
├── Source Brief
├── Knowledge / Prompt / Workflow versions
├── Script package
├── Thumbnail package
├── Quality status
├── Human review status
└── Handoff metadata
```

## Architecture Result

**PASS** — Automation architecture is complete enough for controlled testing.

This is not a claim that a specific external automation platform has been production-validated.