# Prompt Protocol

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Standard Flow

```text
Task Definition
 ↓
Knowledge Selection
 ↓
Context Definition
 ↓
Constraint Definition
 ↓
Output Contract
 ↓
Prompt Construction
 ↓
Test
 ↓
Evaluation
 ↓
Version / Release
```

## Required Components

1. Objective
2. Role / Operating Context when needed
3. Input definition
4. Relevant Knowledge
5. Constraints
6. Procedure / reasoning requirements
7. Output format
8. Quality criteria
9. Failure / uncertainty behavior

## Prompt Design Rules

- ใช้คำสั่งที่ชัดเจนและตรวจสอบได้
- ไม่ใส่ข้อมูลที่ไม่จำเป็น
- แยก Input จาก Instruction
- ระบุสิ่งที่ห้ามทำเมื่อมีความเสี่ยงต่อคุณภาพ
- ให้ระบบระบุความไม่แน่นอนแทนการเดา

## Completion Gate

```text
[ ] Objective clear
[ ] Inputs defined
[ ] Knowledge traceable
[ ] Constraints clear
[ ] Output contract clear
[ ] Quality criteria testable
[ ] Failure behavior defined
[ ] Version recorded
```