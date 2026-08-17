# Versioning Policy

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Versioned Artifacts

ควร Version อย่างชัดเจนเมื่อมีผลต่อ Output:

- Constitution
- Research / Evidence
- Knowledge
- Prompt
- Workflow
- Script
- Thumbnail
- Automation
- Operational configuration

## Semantic Meaning

### MAJOR
เปลี่ยน Contract หรือ behavior สำคัญจน compatibility เดิมอาจใช้ไม่ได้

### MINOR
เพิ่มความสามารถหรือปรับปรุงโดยยังรักษา Contract หลัก

### PATCH
แก้ไขเล็กน้อยหรือข้อผิดพลาดโดยไม่เปลี่ยน behavior สำคัญ

## Traceability

Output สำคัญควรระบุ dependency versions ที่ใช้สร้าง Output นั้น

## Deprecation

Artifact ที่ไม่ควรใช้ต่อให้เปลี่ยนสถานะเป็น `DEPRECATED` และระบุ replacement เมื่อมี