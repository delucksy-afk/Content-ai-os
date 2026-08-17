# Knowledge Protocol

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## 1. Purpose

กำหนดกระบวนการเปลี่ยน Research Output ให้เป็น Knowledge Entry ที่นำกลับมาใช้ได้

## 2. Standard Flow

```text
Research Output
 ↓
Eligibility Check
 ↓
Extract Claims
 ↓
Normalize
 ↓
Classify
 ↓
Attach Sources
 ↓
Quality Check
 ↓
Create Entry
 ↓
Connect
 ↓
Review / Update
```

## 3. Eligibility Gate

ก่อนสร้าง Entry ต้องตรวจ:

- Evidence เพียงพอ
- Source ตรวจสอบได้
- Scope ชัดเจน
- Claim ไม่เกิน Evidence
- มี Use Case
- ไม่ใช่ข้อมูลชั่วคราวที่ควรอยู่เฉพาะ Research

## 4. Normalize

ปรับข้อมูลให้เป็นรูปแบบมาตรฐานโดยไม่เปลี่ยนความหมาย

ต้องแยก:

- Fact
- Inference
- Interpretation
- Recommendation

## 5. Classification

ทุก Entry ควรมี Topic, Type, Tags และ Domain ที่เหมาะสม

## 6. Traceability

Entry สำคัญต้องย้อนกลับได้:

```text
Knowledge Entry → Research ID → Evidence → Source
```

## 7. Reuse

Knowledge ต้องเขียนในลักษณะที่ระบบ Prompt, Workflow และ Content สามารถนำไปใช้ต่อได้โดยไม่ต้องอ่าน Research ทั้งชุดทุกครั้ง

## 8. Update Rule

เมื่อ Source เปลี่ยนหรือ Knowledge หมดอายุ ต้อง:

1. ตรวจผลกระทบ
2. Update Entry หรือ Mark Deprecated
3. บันทึกเหตุผล
4. ตรวจ Downstream Dependencies หากมี

## 9. Quality Gate

```text
[ ] Validated source
[ ] Clear claim
[ ] Context included
[ ] Traceable
[ ] Reusable
[ ] Correct classification
[ ] Freshness handled
```

## 10. Version

**Knowledge Protocol v0.1**