# 09 Operations / Governance

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Purpose

Operations / Governance คือ Control Layer สำหรับดูแล Content AI OS หลังระบบเริ่มทำงานจริง ให้ระบบมีเจ้าของ มีรอบ Review มีการจัดการ Change / Incident / Cost / Health และสามารถตรวจสอบย้อนกลับได้

## Core Loop

```text
RUN
 ↓
OBSERVE
 ↓
REVIEW
 ↓
DECIDE
 ├── KEEP
 ├── IMPROVE
 ├── ROLLBACK
 ├── SUSPEND
 └── DEPRECATE
```

## Scope

- Governance
- Versioning
- Change Management
- Incident Management
- Metrics
- Cost Control
- System Health
- Review Cycle
- Ownership
- Risk Register

## Principle

Operations ไม่ควรแก้ปัญหาเฉพาะหน้าอย่างเดียว แต่ต้องเปลี่ยนเหตุการณ์ที่เกิดขึ้นให้กลายเป็นข้อมูลสำหรับปรับปรุงระบบอย่างมีหลักฐาน

## Status

Operations / Governance v0.1 — ACTIVE