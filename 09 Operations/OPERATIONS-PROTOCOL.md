# Operations Protocol

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Standard Operating Loop

```text
Detect
 ↓
Classify
 ↓
Assess Impact
 ↓
Decide
 ↓
Act
 ↓
Verify
 ↓
Record
 ↓
Learn
```

## Required Questions

ทุกเหตุการณ์สำคัญควรตอบให้ได้:

1. เกิดอะไรขึ้น
2. กระทบอะไร
3. ตรวจพบอย่างไร
4. ใคร / อะไรเป็น Owner
5. การแก้ไขคืออะไร
6. ผลหลังแก้เป็นอย่างไร
7. ต้องเปลี่ยนระบบเพื่อป้องกันซ้ำหรือไม่

## Escalation

Critical incident, security issue, data integrity issue หรือ repeated production failure ต้องหยุด Automation ที่เกี่ยวข้องและส่งต่อ Human Decision

## Evidence Rule

การตัดสินใจเชิงระบบควรอ้างอิง Run logs, Test results, Metrics, Incident records หรือหลักฐานที่ตรวจสอบได้ ไม่ใช้ความรู้สึกเพียงอย่างเดียว