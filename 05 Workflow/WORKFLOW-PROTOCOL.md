# Workflow Protocol

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Standard Flow

```text
Goal Definition
 ↓
Input Definition
 ↓
Stage Design
 ↓
Dependencies
 ↓
Decision Gates
 ↓
Execution
 ↓
Quality Check
 ↓
Handoff
 ↓
Review
```

## Required Components

1. Goal
2. Trigger
3. Inputs
4. Stages
5. Dependencies
6. Decisions
7. Actors / Tools
8. Outputs
9. Quality Gates
10. Failure / Exception Paths
11. Handoff
12. Metrics

## Stage Contract

ทุก Stage ควรระบุ:

- Input
- Action
- Owner / Actor
- Tool / Prompt หากมี
- Output
- Success Criteria
- Failure Path

## Completion Gate

```text
[ ] Goal clear
[ ] Trigger defined
[ ] Inputs defined
[ ] Stages defined
[ ] Decisions defined
[ ] Outputs defined
[ ] Quality gates defined
[ ] Failure paths defined
[ ] Handoff defined
[ ] Metrics defined
```