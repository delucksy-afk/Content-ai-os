# 15 Public Web Layer

**สถานะ:** BUILDING — DOMAIN MIGRATION
**เวอร์ชัน:** v0.1

## Decision

`gmterminal.today` จะถูกนำมาใช้เป็น Public Web Layer ของ Content AI OS

เว็บไซต์เดิมใน repository `delucksy-afk/gmterminal` ไม่ได้ใช้งานจริงตามที่เจ้าของระบบยืนยันแล้ว จึงไม่จำเป็นต้องรักษา UI / Business Logic เดิมไว้เป็นส่วนหนึ่งของระบบใหม่

## Repository Boundary

```text
Content-ai-os
└── Public Web Layer
    └── web/

n8n
└── Runtime / Orchestration

gmterminal.today
└── Public Domain
```

GitHub `Content-ai-os` ยังคงเป็น Source of Truth ของ Architecture, Policy, Runtime Specification และ Public Web source

## Target Architecture

```text
gmterminal.today
      │
      ▼
Public Web
      │
      ▼
Scoped / Authenticated API boundary
      │
      ▼
n8n Runtime
      │
      ▼
Content AI OS Core
```

## Migration Policy

- ไม่เก็บเว็บไซต์ Trading เดิมไว้ใน Public Web ใหม่
- ไม่ย้าย secrets ไป frontend
- ไม่ให้ frontend เรียก privileged APIs โดยตรง
- เริ่มด้วย staging deployment ก่อนเปลี่ยน DNS
- เมื่อ staging ผ่าน จึงชี้ `gmterminal.today` มายัง Public Web ใหม่
- หลัง DNS migration สำเร็จและยืนยันการทำงานแล้ว จึง archive/remove repository เดิมตามขั้นตอน cleanup

## Current Web Source

`web/` คือ source สำหรับ Public Web v0.1

## DNS Gate

DNS ยังต้องเปลี่ยนที่ผู้ให้บริการ DNS/Hosting ของโดเมน เพราะ GitHub connector ไม่ได้มีสิทธิ์จัดการ DNS provider ของผู้ใช้โดยตรง

ก่อน cutover ต้องยืนยัน:

1. HTTPS
2. Desktop / mobile
3. DNS target
4. Public/Private repository behavior
5. API boundary
6. No exposed secrets
7. Rollback path
