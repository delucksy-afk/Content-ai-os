# Verification Protocol — กระบวนการตรวจสอบ

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1  
**อ้างอิง:** `01 Constitution/QUALITY-STANDARD.md`

---

## 1. Purpose

กำหนดวิธีตรวจสอบ Evidence และ Claims ก่อนนำ Research Output ไปใช้งานต่อ

---

## 2. Verification Levels

### Level 0 — Basic

ตรวจว่า Source มีอยู่จริงและ Claim ตรงกับเนื้อหาใน Source

### Level 1 — Context

ตรวจบริบท วันที่ Definition และเงื่อนไขของข้อมูล

### Level 2 — Cross-check

เปรียบเทียบกับ Source อื่นที่เป็นอิสระหรือมีคุณภาพเหมาะสม

### Level 3 — High-risk Review

ใช้เมื่อ Claim มีความเสี่ยงสูง ผลกระทบสูง หรือมีความขัดแย้งสำคัญ และต้องมี Human Review ตามความเหมาะสม

---

## 3. Verification Questions

ก่อนยอมรับ Claim ให้ถาม:

1. Source มีอยู่จริงหรือไม่?
2. Source กล่าวสิ่งนี้จริงหรือไม่?
3. เราตีความเกิน Source หรือไม่?
4. วันที่ยังเหมาะสมหรือไม่?
5. Definition ตรงกันหรือไม่?
6. มีเงื่อนไขหรือข้อจำกัดอะไร?
7. มี Source ที่ขัดแย้งหรือไม่?
8. Confidence สอดคล้องกับ Evidence หรือไม่?

---

## 4. Numerical Verification

สำหรับตัวเลขให้ตรวจ:

- หน่วย
- ช่วงเวลา
- ฐานที่ใช้คำนวณ
- การปัดเศษ
- Denominator
- วันที่เก็บข้อมูล

ห้ามเปรียบเทียบตัวเลขโดยไม่ตรวจว่าใช้ Definition และช่วงเวลาเดียวกันหรือไม่

---

## 5. Temporal Verification

ข้อมูลที่เปลี่ยนแปลงตามเวลา ต้องตรวจวันที่ให้ชัดเจน

หากข้อมูลปัจจุบันแตกต่างจากข้อมูลเดิม ให้เก็บบริบทของช่วงเวลาแทนการเลือกข้อมูลที่ใหม่กว่าโดยอัตโนมัติ

---

## 6. Conflict Verification

เมื่อ Source ขัดแย้งกัน:

```text
ตรวจ Source
   ↓
ตรวจเวลา
   ↓
ตรวจ Definition
   ↓
ตรวจ Methodology
   ↓
ตรวจ Population / Scope
   ↓
ตรวจ Bias / Independence
   ↓
สรุปหรือรายงาน Conflict
```

---

## 7. Verification Record

สำหรับ Claim สำคัญควรบันทึก:

- Claim
- Evidence
- Source
- Verification Level
- Verification Result
- Reviewer
- Date
- Remaining Uncertainty

---

## 8. Failure States

หากตรวจสอบไม่ผ่าน:

- ห้ามใช้ Claim เป็น Verified
- ลด Confidence
- แก้ Claim ให้ตรงกับ Evidence
- ค้นหา Evidence เพิ่ม
- หรือส่ง Human Review

---

## 9. Verification Gate

```text
[ ] Source มีอยู่จริง
[ ] Claim ตรง Source
[ ] Context ถูกต้อง
[ ] Time / Definition ถูกต้อง
[ ] Conflict ได้รับการตรวจ
[ ] Confidence เหมาะสม
[ ] Citation Trace ได้
```

---

## 10. Version

**Verification Protocol v0.1**