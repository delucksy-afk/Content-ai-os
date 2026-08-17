# 03 Knowledge

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1  
**อ้างอิง:** `01 Constitution/` และ `02 Research/`

---

## Purpose

Knowledge คือระบบกลางสำหรับเปลี่ยน Research ที่ผ่านการตรวจสอบแล้วให้เป็นความรู้ที่มีโครงสร้าง ค้นหาได้ เชื่อมโยงได้ และนำกลับมาใช้ซ้ำได้

Knowledge ไม่ใช่คลังข้อมูลทุกอย่าง และไม่ใช่สำเนา Research

---

## Core Principle

> เก็บสิ่งที่มีคุณค่าต่อการใช้งานซ้ำ ไม่ใช่เก็บทุกสิ่งที่ค้นพบ

---

## Knowledge Flow

```text
02 Research
     ↓
Extraction
     ↓
Normalization
     ↓
Classification
     ↓
Quality Check
     ↓
Knowledge Entry
     ↓
Link / Connect
     ↓
Retrieve / Reuse
```

---

## What Belongs in Knowledge

ควรเก็บเมื่อข้อมูล:

- ผ่าน Research หรือมี Source ที่เหมาะสม
- มีประโยชน์ต่อการใช้งานซ้ำ
- มีบริบทเพียงพอ
- สามารถตรวจสอบย้อนกลับได้
- มีอายุการใช้งานที่เหมาะสม หรือมีวิธีจัดการการหมดอายุ

## What Does Not Belong

ไม่ควรเก็บเป็น Permanent Knowledge หากเป็น:

- Search result ชั่วคราว
- Claim ที่ยังไม่ผ่าน Verification
- ความคิดเห็นส่วนตัวที่ไม่มีบริบท
- ข้อมูลซ้ำโดยไม่มีคุณค่าเพิ่ม
- Draft ที่ยังไม่มีการตรวจ

---

## Relationship

```text
Constitution
     ↓
Research
     ↓
Knowledge
     ↓
Prompt / Workflow / Script / Thumbnail / Automation
```

Knowledge เป็นชั้นกลางระหว่าง Evidence และการสร้างงาน

---

## Status

Knowledge v0.1 — ACTIVE