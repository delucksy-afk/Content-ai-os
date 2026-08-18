# 13 Runtime Foundation

**สถานะ:** ACTIVE — DESIGN READY  
**เวอร์ชัน:** v0.1

## Purpose

แปลง Architecture ของ Content AI OS ให้พร้อมเชื่อมต่อ Runtime จริง โดยกำหนด Environment, Integrations, Secrets Boundary, Run Identity, Artifact Storage, Logging, Test Data และ Deployment / Rollback Boundary

## Scope

- Runtime environments
- Tool / API registry
- Integration contracts
- Secret management boundary
- Run ID / correlation ID
- Artifact storage
- Logging / observability
- Test data
- End-to-end contract testing
- Deployment and rollback

## Runtime Decision

`n8n` ถูกเลือกเป็น Orchestration Layer ตัวแรกสำหรับ `VS-001` โดยรายละเอียดการตัดสินใจอยู่ที่ `14 Runtime Implementation/STACK-DECISION.md`

## Public Web Boundary

`gmterminal.today` ถูกกำหนดเป็น Public Web / User Interface candidate ของระบบในระยะ v0.1 โดยยัง **ไม่มีการเปลี่ยน DNS หรือ Hosting target** จนกว่าจะผ่าน Domain Migration Gate

## Non-Goals

ยังไม่ถือว่า Production Ready จนกว่าจะผ่าน Runtime Validation และไม่ให้ Public Web Layer เป็น Source of Truth ของระบบ

## Runtime Flow

```text
Trigger
 ↓
Create Run ID
 ↓
Load Versioned Inputs
 ↓
Execute Workflow
 ↓
Capture Events
 ↓
Validate Outputs
 ↓
Persist Artifacts / Metrics
 ↓
Quality Gate
 ↓
Release / Reject / Rollback
```

## Security Principle

Credentials และ secrets ต้องอยู่นอก Source Code และ Logs; ใช้ least privilege และแยกสิทธิ์ตาม Environment
