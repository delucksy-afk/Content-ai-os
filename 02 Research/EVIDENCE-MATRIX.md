# Evidence Matrix — ตารางควบคุม Evidence

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1  
**อ้างอิง:** `01 Constitution/EVIDENCE-POLICY.md`

---

## 1. Purpose

ใช้บันทึกความสัมพันธ์ระหว่าง Claim, Evidence และ Source เพื่อให้สามารถตรวจสอบย้อนกลับได้

---

## 2. Standard Record

| ID | Claim | Evidence | Source | Source Type | Directness | Confidence | Limitations |
|---|---|---|---|---|---|---|---|
| E-001 |  |  |  |  |  |  |  |

---

## 3. Claim Status

กำหนดสถานะของ Claim เป็น:

- **Verified** — มี Evidence เพียงพอตามเกณฑ์ที่ใช้
- **Supported** — มี Evidence สนับสนุนแต่ยังมีข้อจำกัด
- **Conflicted** — มี Evidence ขัดแย้งกัน
- **Unverified** — ยังไม่มี Evidence เพียงพอ
- **Hypothesis** — เป็นข้อเสนอหรือสมมติฐานที่ยังต้องตรวจสอบ

---

## 4. Evidence Status

Evidence ต้องแยกจากการตีความของ Researcher

```text
Source
  ↓
Observed Evidence
  ↓
Claim
  ↓
Interpretation
```

ห้ามข้ามขั้นโดยทำให้ Interpretation ดูเหมือนเป็นข้อความจาก Source

---

## 5. Directness

ระดับความตรงของ Evidence:

- **Direct** — Source ระบุหรือวัดสิ่งนั้นโดยตรง
- **Indirect** — ต้องอนุมานจากข้อมูล
- **Contextual** — ใช้เพื่อให้บริบท ไม่ได้พิสูจน์ Claim โดยตรง

---

## 6. Confidence

### High

Evidence แข็งแรง Source เหมาะสม และไม่มี Conflict สำคัญ

### Medium

มี Evidence ที่เหมาะสม แต่มีข้อจำกัดหรือยังมีความไม่แน่นอน

### Low

Evidence จำกัด มี Conflict หรือ Source มีข้อจำกัดมาก

### Unknown

ข้อมูลไม่เพียงพอที่จะประเมิน

---

## 7. Conflict Handling

หาก Evidence ขัดแย้งกัน ต้องเก็บ Evidence ทั้งสองด้านและบันทึก:

- Claim ที่ขัดแย้ง
- Source แต่ละด้าน
- เหตุผลที่อาจทำให้ผลต่างกัน
- ข้อจำกัด
- สถานะปัจจุบัน

ไม่ลบ Evidence เพียงเพราะไม่ตรงกับข้อสรุปที่ต้องการ

---

## 8. Traceability

ทุก Claim ที่สำคัญใน Research Output ควรย้อนกลับมายัง Evidence และ Source ได้

```text
Output Claim
     ↓
Evidence ID
     ↓
Source
     ↓
Original Context
```

---

## 9. Minimum Evidence Rule

ไม่มีจำนวน Source ที่ตายตัวสำหรับทุกคำถาม

จำนวนและคุณภาพ Evidence ต้องเหมาะกับ:

- ความสำคัญของ Claim
- ความเสี่ยง
- ความซับซ้อน
- ความขัดแย้ง
- ความสดใหม่ของข้อมูล

---

## 10. Review Checklist

```text
[ ] Claim ชัดเจน
[ ] Evidence ตรงกับ Claim
[ ] Source ตรวจสอบได้
[ ] Context ไม่ถูกบิดเบือน
[ ] Directness ถูกระบุ
[ ] Conflict ถูกบันทึก
[ ] Confidence มีเหตุผลรองรับ
[ ] สามารถ Trace กลับ Source ได้
```

---

## 11. Version

**Evidence Matrix v0.1**