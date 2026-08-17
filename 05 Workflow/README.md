# 05 Workflow Design

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1  
**อ้างอิง:** `01 Constitution/`, `02 Research/`, `03 Knowledge/`, `04 Prompt/`

## Purpose

Workflow คือระบบที่นำ Knowledge, Prompt, Human Decision และ Tool/Automation มาประกอบเป็นกระบวนการทำงานที่ทำซ้ำได้

Workflow ไม่ใช่แค่รายการขั้นตอน แต่ต้องระบุ Input, State, Decision, Output, Owner และ Failure Path

## Flow

```text
Goal
 ↓
Input
 ↓
Stages
 ↓
Decision Gates
 ↓
Prompt / Human / Tool
 ↓
Output
 ↓
Quality Check
 ↓
Handoff
```

## Principles

- ทุก Workflow ต้องมีจุดเริ่มต้นและจุดสิ้นสุด
- แต่ละ Stage ต้องมี Input และ Output
- Decision สำคัญต้องมีเกณฑ์ ไม่ใช้ความรู้สึกล้วน
- Failure และ Exception ต้องมีทางออก
- Human-in-the-loop ต้องระบุเมื่อจำเป็น
- Workflow ต้องสามารถวัดและปรับปรุงได้

## Status

Workflow Design v0.1 — ACTIVE