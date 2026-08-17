# Runtime Architecture

**เวอร์ชัน:** v0.1

## Environments

```text
DEV
 ↓
TEST
 ↓
STAGING
 ↓
PRODUCTION
```

Promotion ต้องผ่าน Quality Gate และไม่ควรใช้ Production credentials ใน Environment ที่ต่ำกว่า

## Runtime Components

1. Trigger
2. Orchestrator
3. AI / external services
4. Artifact store
5. Event / metrics capture
6. Quality gate
7. Human review where required
8. Release / rollback controller

## Run Identity

ทุก Production execution ควรมี `run_id` และเชื่อมกับ Content ID และ Version IDs ที่เกี่ยวข้อง

## Failure Boundary

Runtime ต้องสามารถหยุดงานได้เมื่อพบ:

- Invalid input
- Contract mismatch
- Repeated failure
- Security violation
- Quality gate failure
- Unbounded retry

## Production Principle

ห้ามถือว่า “Automation completed” = “Content approved” โดยอัตโนมัติ