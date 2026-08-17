# Deployment & Rollback Boundary

**สถานะ:** ACTIVE — DESIGN

## Promotion

```text
DEV
 ↓
TEST
 ↓
STAGING
 ↓
PRODUCTION
```

แต่ละ Promotion ต้องมี:

- Version
- Change record
- Test result
- Approval / gate where required
- Rollback plan

## Rollback Triggers

- Critical quality regression
- Security issue
- Data integrity issue
- Unbounded automation behavior
- Unexpected cost / usage spike
- Contract-breaking change

## Rollback Principle

Rollback ต้องคืนระบบไปยัง Version ที่ทราบว่าใช้งานได้ โดยไม่ทำลาย historical evidence หรือ audit records

## No-Deploy Rule

หากไม่มี test evidence หรือ rollback path ที่เหมาะสม ห้ามประกาศ Production deployment ว่าพร้อม