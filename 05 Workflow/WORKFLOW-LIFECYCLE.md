# Workflow Lifecycle

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

## Review Triggers

- Input เปลี่ยน
- Prompt / Knowledge dependency เปลี่ยน
- Tool เปลี่ยน
- Failure rate สูงขึ้น
- Output quality ลดลง
- Requirement เปลี่ยน
- Automation ถูกเพิ่มเข้ามา

ทุกการเปลี่ยนแปลงสำคัญต้องบันทึก Version และผลกระทบ