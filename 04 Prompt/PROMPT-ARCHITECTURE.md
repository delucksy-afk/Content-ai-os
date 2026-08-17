# Prompt Architecture

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Layers

```text
L1 Objective
L2 Context
L3 Knowledge
L4 Instructions
L5 Constraints
L6 Output Contract
L7 Quality Criteria
L8 Evaluation
```

## Separation of Concerns

- Objective บอกว่าต้องการผลลัพธ์อะไร
- Context บอกสถานการณ์และข้อมูลแวดล้อม
- Knowledge ให้ข้อมูลอ้างอิงที่ผ่านการจัดการ
- Instructions บอกวิธีทำงาน
- Constraints กำหนดขอบเขต
- Output Contract กำหนดหน้าตาผลลัพธ์
- Quality Criteria กำหนดว่าอะไรถือว่าดี
- Evaluation ตรวจผลลัพธ์จริง

## Prompt vs Knowledge

Prompt ควรอ้างอิง Knowledge แทนการทำหน้าที่เป็นฐานความรู้ถาวร

หากข้อมูลหนึ่งถูกใช้ซ้ำในหลาย Prompt และมีแหล่งอ้างอิง ควรพิจารณาย้ายไป `03 Knowledge`

## Versioning

การเปลี่ยน Objective, Instruction, Constraint หรือ Output Contract ที่อาจเปลี่ยนพฤติกรรม ต้องเพิ่ม Version หรือบันทึก Change อย่างชัดเจน