# Workflow Design Rules

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## 1. Start With Outcome

ออกแบบจากผลลัพธ์ย้อนกลับ ไม่ใช่เริ่มจากเครื่องมือที่อยากใช้

## 2. Minimize Unnecessary Steps

ทุก Stage ต้องมีเหตุผลหรือ Value ต่อ Output

## 3. Explicit Decisions

Decision ที่ส่งผลต่อคุณภาพต้องมีเกณฑ์หรือ Evidence ที่เกี่ยวข้อง

## 4. Preserve Traceability

เมื่อ Workflow ใช้ Knowledge หรือ Prompt สำคัญ ต้องบันทึก ID / Version ที่ใช้

## 5. Design For Failure

ทุกจุดสำคัญต้องพิจารณา Missing Input, Invalid Output, Tool Failure และ Human Rejection

## 6. Human Review

กำหนด Human Review เมื่อผลลัพธ์มีความเสี่ยงสูง คลุมเครือ หรือมีผลกระทบที่ไม่ควรปล่อยอัตโนมัติ

## 7. Idempotency Where Possible

หากรันซ้ำได้ ควรหลีกเลี่ยงการสร้างผลซ้ำหรือทำข้อมูลเสียหาย

## 8. Observability

เก็บข้อมูลที่จำเป็นต่อการรู้ว่า Workflow สำเร็จหรือพังตรงไหน

## 9. Change Control

การเปลี่ยน Stage, Decision Gate หรือ Output Contract ที่มีนัยสำคัญต้องเพิ่ม Version