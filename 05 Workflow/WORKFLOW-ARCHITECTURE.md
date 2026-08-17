# Workflow Architecture

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Layers

```text
L1 Goal / Trigger
L2 Input
L3 Process Stages
L4 Decision Gates
L5 Execution Units
L6 Quality Gates
L7 Output / Handoff
L8 Metrics / Feedback
```

## Execution Unit Types

- Human Decision
- Prompt
- Tool
- Automation
- External Service
- Review

## State

Workflow ควรรู้ว่า Item อยู่ขั้นใด เช่น:

```text
NEW → IN_PROGRESS → REVIEW → APPROVED → COMPLETE
                         ↘ REWORK
```

## Dependency Direction

```text
Knowledge → Prompt → Workflow
```

Workflow อาจเรียก Prompt หลายตัว แต่ไม่ควรทำหน้าที่เป็น Knowledge Store

## Design Rule

หากขั้นตอนหนึ่งมี Logic ซับซ้อนและนำกลับมาใช้ซ้ำได้ ให้แยกเป็น Component แทนการฝังไว้ใน Workflow เดียว