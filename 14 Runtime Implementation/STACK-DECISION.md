# Initial Stack Decision

**Status:** DECISION PENDING — criteria established

## Principle

อย่าเลือกเครื่องมือเพราะเป็นของยอดนิยม ให้เลือกจากความเหมาะสมกับ Content AI OS และความสามารถในการตรวจสอบย้อนหลัง

## Evaluation Criteria

| Criterion | Weight | Question |
|---|---:|---|
| Integration fit | High | เชื่อม Workflow / AI / Storage ได้หรือไม่ |
| Observability | High | ตรวจ Run / Error / Cost ได้หรือไม่ |
| Versionability | High | เปลี่ยนและย้อน Version ได้หรือไม่ |
| Security | High | Secret / Permission ควบคุมได้หรือไม่ |
| Reliability | High | Retry / Timeout / Failure control ดีหรือไม่ |
| Cost | Medium | เหมาะกับระยะทดลองหรือไม่ |
| Portability | Medium | ย้ายออกได้หรือไม่ |
| Simplicity | High | ดูแลคนเดียวได้หรือไม่ |

## Decision Rule

เลือก Stack ที่ทำให้ Vertical Slice `VS-001` ผ่านได้ด้วยความซับซ้อนต่ำที่สุด โดยไม่ลด Security, Traceability หรือ Quality Controls

## Current Decision

**ยังไม่ lock vendor**

ขั้นถัดไปคือระบุเครื่องมือที่ผู้ใช้มีอยู่แล้ว และตรวจ permissions ก่อนเลือก integration จริง