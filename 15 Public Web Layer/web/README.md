# Public Web v0.1

## Purpose

หน้าเว็บสาธารณะของ Content AI OS สำหรับ `gmterminal.today`

## Current State

- Static shell only
- No privileged API calls
- No secrets
- No authentication
- No automatic publishing
- Runtime remains in n8n

## Deployment

นำโฟลเดอร์ `web/` ไป deploy บน hosting ที่รองรับ static site ได้

## Domain

Target domain: `gmterminal.today`

DNS cutover ต้องทำที่ผู้ให้บริการ DNS/hosting ของโดเมน หลังจาก staging ผ่านเท่านั้น

## Security Boundary

Frontend ห้ามถือ API keys หรือเรียก privileged services โดยตรง

เมื่อมี Backend/API จะต้องอยู่หลัง scoped/authenticated boundary และ n8n จะเป็น orchestration layer ตาม Architecture v0.1