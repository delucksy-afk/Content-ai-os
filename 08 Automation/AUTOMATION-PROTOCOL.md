# Automation Protocol

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Standard Lifecycle

```text
Trigger
 ↓
Input Validation
 ↓
Dependency Resolution
 ↓
Execution
 ↓
Validation
 ↓
Human Gate if required
 ↓
Commit / Persist
 ↓
Handoff
 ↓
Logging
```

## Required Controls

- Explicit Trigger
- Input Contract
- Output Contract
- Dependency Version
- Timeout / Retry Policy
- Failure Path
- Human Review Policy
- Idempotency Strategy
- Logging
- Audit Trail where appropriate

## Stop Conditions

Automation ต้องหยุดหรือส่งให้มนุษย์เมื่อ:

- Input ไม่ครบหรือผิดรูปแบบ
- Confidence / validation ต่ำกว่าเกณฑ์ที่กำหนด
- พบ Policy / Ethics risk
- Dependency unavailable
- เกิด repeated failure
- Output contract ไม่ผ่าน

## No Silent Failure

ห้ามทำให้ระบบดูเหมือนสำเร็จเมื่อ Output ไม่ได้ถูกสร้างหรือ Validation ไม่ผ่าน