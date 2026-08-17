# Automation Architecture

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Layers

```text
L1 Trigger
L2 Orchestration
L3 Input / Output Contracts
L4 Tools / Services
L5 State / Persistence
L6 Validation / Quality Gates
L7 Human Review
L8 Logging / Metrics
L9 Recovery
```

## Architecture Rule

```text
Workflow defines WHAT and WHEN
Automation defines HOW the system executes it
```

Automation ไม่ควรเป็นแหล่งความรู้หลัก และไม่ควรฝัง Business Logic ซ้ำกับ Workflow โดยไม่จำเป็น

## State

อย่างน้อยควรติดตาม:

```text
QUEUED
RUNNING
WAITING_REVIEW
SUCCEEDED
FAILED
RETRYING
CANCELLED
```

## Dependency Boundary

External services ต้องถูกระบุเป็น Dependency และไม่ควรถือว่า availability เป็นสิ่งรับประกันตลอดเวลา