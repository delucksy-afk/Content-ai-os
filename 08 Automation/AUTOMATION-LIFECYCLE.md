# Automation Lifecycle

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

```text
Idea
 ↓
Prototype
 ↓
Tested
 ↓
Production
 ↓
Monitored
 ├── Improve
 ├── Rollback
 ├── Suspend
 └── Deprecated
```

## Change Triggers

- Workflow changed
- Prompt / Knowledge dependency changed
- Tool / API changed
- Error rate changed
- Security issue
- Cost changed materially
- Requirement changed

การเปลี่ยนแปลงที่มีผลต่อ Output ต้องบันทึก Version และผลกระทบ