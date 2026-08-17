# Prompt Lifecycle

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

```text
Idea
 ↓
Draft
 ↓
Tested
 ↓
Production
 ↓
Monitored
 ├── Revised
 ├── Superseded
 └── Deprecated
```

## Triggers

ทบทวน Prompt เมื่อ:

- Model เปลี่ยน
- Knowledge เปลี่ยน
- Task เปลี่ยน
- Output quality ลดลง
- พบ Failure Pattern
- มี Requirement ใหม่

ทุกการเปลี่ยนแปลงที่มีนัยสำคัญต้องบันทึก Version และเหตุผล