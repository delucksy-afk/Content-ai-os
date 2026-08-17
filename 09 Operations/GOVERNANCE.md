# Governance

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Governance Principles

- Single source of truth สำหรับสถานะระบบ
- ทุก Production change ต้อง trace ได้
- Risk สูงต้องมี Human approval
- Deprecated artifact ต้องไม่ถูกใช้โดยไม่ตั้งใจ
- Decision สำคัญต้องมีเหตุผลและหลักฐาน

## Ownership

แต่ละ System Component ควรมี Owner อย่างน้อยหนึ่งคนหรือหนึ่งบทบาท:

- Constitution Owner
- Research / Knowledge Owner
- Prompt Owner
- Workflow Owner
- Production Owner
- Automation Owner
- Operations Owner

ในระยะเริ่มต้นคนเดียวสามารถรับหลายบทบาทได้ แต่ Owner ต้องชัดเจน

## Decision Classes

### Routine
ทำตาม Standard ได้ ไม่ต้อง Escalate

### Controlled
ต้อง Review ก่อน Release

### Critical
กระทบ Security, Ethics, Data Integrity หรือ Production ต้องมี Explicit Approval

## Governance Records

- Decision Log
- Change Request
- Incident Record
- Release Record
- Review Record
- Risk Register