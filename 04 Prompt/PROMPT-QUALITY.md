# Prompt Quality Standard

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Quality Dimensions

- Clarity — คำสั่งไม่กำกวม
- Relevance — ใช้ Context และ Knowledge ที่เกี่ยวข้อง
- Completeness — มีองค์ประกอบที่จำเป็น
- Controllability — Output อยู่ในขอบเขตที่กำหนด
- Consistency — ทำงานได้สม่ำเสมอเมื่อ Input ใกล้เคียงกัน
- Traceability — รู้ว่า Knowledge ใดถูกใช้
- Evaluability — มีวิธีตัดสินผลลัพธ์
- Maintainability — แก้ไขและ Version ได้ง่าย

## Quality Levels

### Draft
ยังไม่ผ่าน Test

### Tested
ผ่าน Test Case ที่กำหนด

### Production
ผ่าน Evaluation และเหมาะกับการใช้งานจริง

### Deprecated
ไม่ควรใช้ต่อ

## Gate

```text
[ ] Clear
[ ] Complete
[ ] Relevant
[ ] Testable
[ ] Traceable
[ ] Maintainable
```