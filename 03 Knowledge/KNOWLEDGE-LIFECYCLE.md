# Knowledge Lifecycle

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

```text
Candidate
   ↓
Validated
   ↓
Active
   ↓
Reviewed
   ├── Updated
   ├── Superseded
   └── Deprecated
```

## Candidate

ผ่านการคัดเลือกเบื้องต้น แต่ยังไม่ผ่าน Quality Gate ครบ

## Validated

ผ่าน Verification และ Quality Gate ที่จำเป็น

## Active

พร้อมใช้งานในระบบ

## Reviewed

ได้รับการตรวจซ้ำตามรอบหรือเมื่อมี Trigger

## Updated

ข้อมูลได้รับการปรับปรุงโดยยังคงใช้ Entry เดิม

## Superseded

มี Knowledge ใหม่ที่แทนที่ Entry เดิม ควรเก็บ Link ไปยัง Entry ใหม่

## Deprecated

ไม่ควรใช้งานอีกต่อไป แต่เก็บประวัติเพื่อ Traceability

## Review Triggers

- Source เปลี่ยน
- กฎหมาย/นโยบายเปลี่ยน
- ข้อมูลหมดอายุ
- พบ Error
- มี Evidence ใหม่ที่สำคัญ
- Downstream system พบปัญหา

## Version

**Knowledge Lifecycle v0.1**