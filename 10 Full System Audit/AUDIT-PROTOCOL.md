# Audit Protocol

## 1. Scope Lock

กำหนด Version / Commit ที่กำลังตรวจ และห้ามเปลี่ยน Scope กลาง Audit โดยไม่มีบันทึก

## 2. Inventory

ตรวจโครงสร้าง `00–09` และรายการ Artifact สำคัญ

## 3. Contract Check

ตรวจว่า Input / Output / Owner / Status / Version ของแต่ละ Layer สอดคล้องกัน

## 4. Traceability Check

ตรวจสายการอ้างอิงตั้งแต่ Research → Knowledge → Prompt → Workflow → Production → Automation → Operations

## 5. Handoff Check

ตรวจว่าทุก Boundary ส่งข้อมูลที่ Layer ถัดไปต้องใช้ครบ

## 6. Gate Check

ตรวจ Quality Gate, Human Gate และ Release Gate

## 7. Risk Check

ตรวจ Security, Privacy, Misleading Content, Failure, Recovery และ Dependency Risk

## 8. Test Check

ตรวจ Test Case และแยก Architecture Test ออกจาก Runtime / Performance Test

## 9. Documentation Check

ตรวจ Naming, Status, Version, Changelog และ Cross-reference

## 10. Findings

ทุก Finding ต้องมี:

- ID
- Severity
- Location
- Observation
- Impact
- Recommendation
- Owner / Next Action

## 11. Decision

หลังแก้ Finding สำคัญ ให้ Re-audit เฉพาะ Scope ที่ได้รับผลกระทบ และบันทึกผล