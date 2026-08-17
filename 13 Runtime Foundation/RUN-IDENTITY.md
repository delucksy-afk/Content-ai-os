# Run Identity

**สถานะ:** ACTIVE — DESIGN

## Required IDs

```text
content_id
run_id
event_id
experiment_id (when applicable)
```

## Version Links

A run should record relevant versions:

```text
constitution_version
knowledge_version
prompt_version
workflow_version
script_version
thumbnail_version
automation_version
```

## Purpose

ทำให้สามารถตอบย้อนหลังได้ว่า:

- Run นี้ทำอะไร
- ใช้ Version ใด
- เกิด Event อะไร
- Output ใดถูกสร้าง
- Metric ใดสัมพันธ์กับ Run
- Experiment ใดเกี่ยวข้อง

## Rule

ห้ามนำ timestamp มาใช้แทน unique run identity เพียงอย่างเดียว