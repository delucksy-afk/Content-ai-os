# Vertical Slice Specification

**ID:** VS-001  
**Status:** READY FOR IMPLEMENTATION

## Objective

สร้าง Content Run ที่ตรวจสอบย้อนกลับได้ตั้งแต่ Input ถึง Evidence โดยไม่ต้องเชื่อมทุกระบบในครั้งเดียว

## Input

- Brief ID
- Content ID
- Knowledge Version
- Prompt Version
- Workflow Version

## Execution

1. Create `run_id`
2. Load exact versions
3. Execute one controlled content generation step
4. Validate output schema
5. Run Quality Gate
6. Persist artifact reference
7. Emit measurement event
8. Create Operations record

## Output

ต้องมีอย่างน้อย:

```text
run_id
content_id
output_artifact_ref
prompt_version
knowledge_version
workflow_version
quality_status
created_at
measurement_event_id
```

## Acceptance Criteria

- Run สามารถ replay / inspect ได้จาก recorded metadata
- ไม่มี secret อยู่ใน output หรือ logs
- Failed quality gate ไม่ถูกนับเป็น successful output
- Event เชื่อมกลับไปยัง run ได้
- Version IDs ตรงกับสิ่งที่ถูกใช้จริง
- มี failure path ที่หยุดงานได้

## Out of Scope

- Full production deployment
- Multi-platform distribution
- Automated self-modifying prompts
- Autonomous optimization
