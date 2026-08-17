# n8n Setup Plan

**สถานะ:** READY — WAITING FOR USER ENVIRONMENT
**Runtime:** n8n
**Version:** v0.1

## Goal

ใช้ n8n เป็น Orchestration Layer ตัวแรกของ Content AI OS โดยเริ่มจาก TEST/DEV และไม่แตะ Production credentials

## Recommended Initial Path

```text
n8n
 ↓
VS-001 Test Input
 ↓
Create run_id
 ↓
Validate input
 ↓
Select versioned prompt/knowledge
 ↓
AI provider call
 ↓
Quality Gate
 ↓
Write artifact reference
 ↓
Write measurement event
 ↓
Return run result
```

## Environment Recommendation

เริ่มจาก **n8n Cloud trial/free availability หากบัญชีและแผนปัจจุบันรองรับ** หรือ self-hosted test instance หากต้องการควบคุมระบบเอง

ก่อนเลือกแบบถาวร ให้เปรียบเทียบ:

- Cost
- Reliability
- Secret management
- Backup
- Maintenance
- Webhook accessibility
- Execution history

## Security

- ใช้ TEST credentials เท่านั้นในช่วงแรก
- ห้ามใส่ secrets ใน workflow JSON ที่ commit เข้า GitHub
- ใช้ n8n Credentials / environment secret mechanism
- จำกัดสิทธิ์ Google / AI APIs ตามงานที่จำเป็น

## First Milestone

ทำให้ workflow `VS-001` สามารถรับ Test Fixture → สร้าง `run_id` → เรียก AI → ตรวจ Quality Gate → ส่งผลลัพธ์กลับมาได้

## Not Yet

- Auto publish to YouTube
- Production credentials
- Autonomous high-risk actions
- Unbounded retries
- Automatic destructive operations