# Workflow Test — W-001

**Workflow ID:** W-2026-08-17-001  
**Version:** v0.1  
**Status:** TESTED  
**Knowledge:** K-2026-08-17-001  
**Prompt:** P-2026-08-17-001

## Goal

เปลี่ยน Topic + Audience + Video Promise ให้เป็นชุด Content Packaging Concepts ที่ตรวจสอบได้และพร้อมส่งต่อไปยัง Script / Thumbnail stages

## Trigger

ได้รับ Brief ของวิดีโอที่มีข้อมูลขั้นต่ำครบ

## Inputs

- Topic
- Target audience
- Video promise
- Tone

หากข้อมูลสำคัญไม่ครบ → `NEEDS_INPUT`

## Dependencies

- Knowledge: K-2026-08-17-001
- Prompt: P-2026-08-17-001

## Stages

| # | Stage | Actor | Output | Gate |
|---|---|---|---|---|
| 1 | Validate Brief | Human / Workflow | Validated Brief | Input complete |
| 2 | Generate Packaging | Prompt P-001 | Title + Thumbnail concepts | Format complete |
| 3 | Misleading Check | Human / Rule | Approved / Rework | No misleading promise |
| 4 | Select Concepts | Human | Selected concepts | Meets brief |
| 5 | Handoff | Workflow | Packaging Package | Ready for next stage |

## Decision Gates

### Gate 1 — Input

Pass → Generate  
Fail → NEEDS_INPUT

### Gate 2 — Quality

Pass → Select  
Fail → REWORK

### Gate 3 — Final

Pass → Handoff  
Fail → REWORK

## State Model

```text
NEW
 ↓
VALIDATED
 ↓
GENERATING
 ↓
REVIEW
 ├── REWORK → GENERATING
 └── APPROVED
       ↓
    COMPLETE
```

## Failure Paths

- Missing input → request missing fields
- Prompt failure → retry / manual fallback
- Misleading claim → rework
- Human rejection → rework with feedback
- Tool failure → record failure and use fallback path if available

## Output Contract

```text
Packaging Package
├── Audience / Intent
├── Title Concepts
├── Thumbnail Concepts
├── Recommended Pairs
├── Risk Check
└── Open Questions
```

## Metrics

- Completion rate
- Rework rate
- Time to approved package
- Human intervention
- Failure count

## Test Cases

### Happy Path
Brief ครบ → Workflow จบที่ COMPLETE

### Missing Input
ไม่มี Audience → NEEDS_INPUT

### Rework
พบ misleading promise → REWORK → Review ใหม่

### Tool Failure
Prompt execution ไม่สำเร็จ → fallback / retry

### Re-run
การรันซ้ำต้องไม่ทำให้ package เดิมเสียหาย และต้องระบุ version ของ dependency

## Evaluation

**Architecture Result:** PASS

เหตุผล: มี Trigger, Input, Dependencies, Stage Contracts, Decision Gates, Failure Paths, Human Review, Output Contract, Handoff และ Metrics ครบตาม Workflow Protocol

## Limitations

ยังเป็น Architecture Test ไม่ใช่ Production performance test
