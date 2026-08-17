# Optimization Protocol

## Standard Cycle

```text
Question
 ↓
Baseline
 ↓
Hypothesis
 ↓
Experiment Design
 ↓
Controlled Change
 ↓
Measure
 ↓
Compare
 ↓
Interpret
 ↓
Decision
 ↓
Version / Record
```

## Required Separation

**Observation:** สิ่งที่ข้อมูลแสดง

**Interpretation:** ความหมายที่เราตีความจากข้อมูล

**Hypothesis:** คำอธิบายที่ยังต้องทดสอบ

**Decision:** สิ่งที่เลือกทำหลังพิจารณาหลักฐาน

## Stop Conditions

หยุด Optimization หาก:

- Data quality ไม่พอ
- Sample / context ไม่เหมาะสมกับข้อสรุป
- Experiment มี Confounder สำคัญที่ควบคุมไม่ได้
- ผลกระทบด้าน Ethics / Truthfulness เพิ่มขึ้น
- Cost / Risk สูงกว่าประโยชน์ที่คาดหมาย

## Change Rule

ผลการทดลองที่มีผลต่อระบบต้องสร้าง Versioned Change และสามารถย้อนกลับได้