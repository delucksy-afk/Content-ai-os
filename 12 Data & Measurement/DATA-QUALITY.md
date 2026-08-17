# Data Quality Standard

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Dimensions

- Accuracy
- Completeness
- Consistency
- Timeliness
- Uniqueness
- Validity
- Traceability

## Quality Gates

```text
Capture
 ↓
Schema Validation
 ↓
Required Field Check
 ↓
Type / Unit Check
 ↓
Duplicate Check
 ↓
Timestamp Check
 ↓
Context Check
 ↓
Accepted / Rejected / Quarantined
```

## Bad Data

หากข้อมูลผิดหรือไม่ครบ:

- ห้าม silently fill ข้อมูลสำคัญ
- แยกเป็น rejected / quarantined record ตามความเหมาะสม
- บันทึกเหตุผล
- แก้ด้วย correction record หากจำเป็น

## Measurement Integrity

ห้ามเปลี่ยน Definition ของ Metric กลาง Time Series โดยไม่ Version Definition เพื่อป้องกันการเปรียบเทียบข้อมูลที่ไม่ใช่สิ่งเดียวกัน