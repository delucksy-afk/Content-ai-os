# Data Architecture

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Layers

```text
L1 Event / Source Data
L2 Raw Capture
L3 Validated Data
L4 Canonical Dataset
L5 Metrics / Derived Data
L6 Experiment Dataset
L7 Decision / Learning Record
```

## Source Categories

- Research evidence
- Content production events
- Workflow / automation events
- Quality review events
- Distribution / platform metrics
- Experiment results
- Operational incidents
- Cost events

## Identity

ทุกข้อมูลสำคัญควรเชื่อมโยงได้อย่างน้อยกับ:

```text
Content ID
Run ID
Workflow Version
Prompt Version
Knowledge Version
Automation Version
Timestamp
```

เมื่อบริบทใดไม่เกี่ยวข้อง ให้ระบุเป็น null / not applicable แทนการเดาข้อมูล

## Source of Truth

Raw source data ควรเก็บแยกจาก Derived Metrics เพื่อให้สามารถตรวจสอบวิธีคำนวณย้อนหลังได้

## Immutability

ข้อมูลเหตุการณ์ที่เกิดขึ้นแล้วไม่ควรถูกแก้ย้อนหลังโดยไม่มี Audit Trail หากต้องแก้ให้สร้าง correction / superseding record