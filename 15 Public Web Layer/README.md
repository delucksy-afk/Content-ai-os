# 15 Public Web Layer

**สถานะ:** PLANNED — DOMAIN MIGRATION GATE  
**เวอร์ชัน:** v0.1

## Purpose

กำหนด Public Web Layer ของ Content AI OS โดยใช้ `gmterminal.today` เป็นโดเมนสาธารณะที่วางไว้หน้าระบบ โดยแยก Public UI ออกจาก Source of Truth และ Runtime

## Current Reality

โดเมนและเว็บไซต์ `gmterminal.today` ปัจจุบันอยู่กับ repository `delucksy-afk/gmterminal` ซึ่งมี `index.html` เป็นเว็บไซต์เดิม ดังนั้นยังไม่ควรเปลี่ยน DNS/Hosting target ทันที

## Target Architecture

```text
gmterminal.today
      │
      ▼
Public Web Layer
      │
      ├── Landing / Dashboard
      ├── Content Operations UI
      └── Runtime Status / Reports
              │
              ▼
          n8n / APIs
              │
              ▼
       Content AI OS Core
              │
              ▼
           GitHub
```

## Boundary

- GitHub = Source of Truth
- n8n = Runtime / Orchestration
- Public Web = Interface / Presentation Layer
- Secrets must remain outside frontend code
- Public Web must not directly expose privileged credentials

## Migration Gate

ห้ามเปลี่ยน DNS หรือ Hosting จนกว่าจะผ่าน:

1. ตรวจเว็บไซต์เดิม
2. ตัดสินใจว่าจะย้าย / เปลี่ยน / แยก subdomain
3. สร้าง Public Web v0.1
4. ทดสอบบน staging URL
5. ตรวจ security และ mobile behavior
6. เตรียม rollback
7. จึงเปลี่ยน DNS

## Recommended Direction

ไม่ merge `gmterminal` repository เข้า `Content-ai-os` โดยตรงใน v0.1 เพราะหน้าที่ต่างกันชัดเจน ให้ `gmterminal` เป็น Web Layer repository และ `Content-ai-os` เป็น OS / Architecture / Runtime Source of Truth ก่อน
