# Cost Control

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Cost Categories

- Model / API usage
- Automation platform
- Storage
- External services
- Human review time

## Controls

- Track measurable cost
- Set budget boundaries where possible
- Detect abnormal usage
- Prefer bounded retries
- Avoid duplicate runs
- Review expensive dependencies

## Cost Decision

Cost ต้องพิจารณาควบคู่กับ Quality, Reliability และ Value ไม่ใช่ลดค่าใช้จ่ายจนระบบคุณภาพตก

## Alert Conditions

ควรตรวจสอบเมื่อ:

- Cost per run สูงผิดปกติ
- Retry สูงขึ้นผิดปกติ
- Duplicate execution เกิดซ้ำ
- External service pricing / quota เปลี่ยน