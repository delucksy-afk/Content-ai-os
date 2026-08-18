# gmterminal.today — Domain Migration Plan

**สถานะ:** APPROVED FOR BUILD — NO DNS CUTOVER YET

## Owner Decision

เจ้าของระบบยืนยันว่าเว็บไซต์เดิมไม่ได้ใช้งานจริง และไม่จำเป็นต้องรักษา UI / Business Logic / Data ของเว็บไซต์เดิมไว้

ดังนั้น `gmterminal.today` สามารถย้ายมาเป็น Public Web ของ Content AI OS ได้โดยตรง

## Current State Verified

Repository `delucksy-afk/gmterminal` มี `index.html` เดิมเพียงไฟล์หลัก และเป็นเว็บไซต์ Trading เดิมที่ไม่ใช่เป้าหมายของ Content AI OS

## Target

```text
gmterminal.today
      ↓
Content AI OS Public Web
      ↓
Scoped / Authenticated API boundary
      ↓
n8n Runtime
      ↓
Content AI OS Core
```

## Migration Decision

**เลือก Direct Replacement**

ไม่จำเป็นต้องใช้ `app.gmterminal.today` เป็นทางผ่านระยะยาว เพราะเจ้าของระบบยืนยันแล้วว่าเว็บไซต์เดิมไม่มีภารกิจที่ต้องรักษาไว้

## Required Sequence

1. Build Public Web v0.1 ใน `Content-ai-os`
2. Deploy staging
3. ตรวจ desktop / mobile / HTTPS
4. ตรวจ API boundary และไม่ให้ frontend เปิดเผย secrets
5. ตั้ง custom domain `gmterminal.today` ให้กับ deployment ใหม่
6. ตรวจ DNS propagation
7. Smoke test หน้าเว็บ
8. เมื่อยืนยันว่าเว็บใหม่ทำงานแล้ว จึง archive/remove เว็บไซต์เดิม

## DNS / Hosting Boundary

การเปลี่ยน DNS ต้องทำที่ผู้ให้บริการ DNS ของโดเมน เพราะ GitHub connector ที่ใช้อยู่ไม่มีสิทธิ์จัดการ DNS provider ของผู้ใช้โดยตรง

## Old Repository Cleanup

`delucksy-afk/gmterminal` ไม่ต้องถูก merge เข้า `Content-ai-os`

หลัง Domain Cutover สำเร็จ:

- archive repository เดิม หรือ
- ลบ repository เดิม หากเจ้าของระบบยืนยันอีกครั้ง

**ห้ามลบก่อนยืนยันว่า Domain ใหม่ทำงานสำเร็จ** เพื่อป้องกัน downtime โดยไม่จำเป็น

## Rollback

Rollback คือการคืน DNS target ไปยัง hosting เดิมก่อนลบ/ทำลายข้อมูลเดิม หากพบปัญหาระหว่าง cutover
