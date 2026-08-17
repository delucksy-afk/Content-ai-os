# Change Management

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Change Flow

```text
Request
 ↓
Assess
 ↓
Plan
 ↓
Approve
 ↓
Implement
 ↓
Test
 ↓
Release
 ↓
Monitor
 ↓
Close / Rollback
```

## Change Assessment

ก่อนเปลี่ยนแปลงให้พิจารณา:

- Scope
- Dependencies
- Risk
- User / Output impact
- Rollback plan
- Test plan
- Cost impact

## Fast Fix

Emergency fix ทำได้เมื่อจำเป็น แต่ต้องบันทึกเหตุผลและทำ Post-change Review ภายหลัง

## No Untracked Change

ห้ามแก้ Production behavior สำคัญโดยไม่มี Version / Record ที่เพียงพอสำหรับย้อนตรวจ