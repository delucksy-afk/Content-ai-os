# 04 Prompt

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1  
**อ้างอิง:** `01 Constitution/`, `03 Knowledge/`

## Purpose

Prompt คือชั้นแปลง Knowledge + Task + Context + Constraints ให้เป็นคำสั่งที่ทำซ้ำได้ ตรวจสอบได้ และประเมินผลได้

Prompt ไม่ใช่เพียงข้อความสั่ง AI แต่เป็นส่วนหนึ่งของระบบการผลิต Output

## Flow

```text
Knowledge
   +
Task
   +
Context
   +
Constraints
   +
Quality Criteria
        ↓
Prompt Specification
        ↓
Prompt
        ↓
Execution
        ↓
Evaluation
        ↓
Revision / Version
```

## Principles

- Prompt ต้องมีวัตถุประสงค์ชัด
- Context ต้องเพียงพอแต่ไม่ฟุ่มเฟือย
- Constraints ต้องตรวจสอบได้
- Output Contract ต้องระบุรูปแบบผลลัพธ์
- Quality Criteria ต้องวัดได้เท่าที่ทำได้
- Prompt สำคัญต้องมี Version และ Test
- Prompt ไม่ควรฝัง Knowledge ที่ควรอยู่ใน Knowledge Layer โดยไม่จำเป็น

## Status

Prompt v0.1 — ACTIVE