# Workflow Evaluation

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Evaluation Dimensions

- Goal completion
- Output quality
- Failure rate
- Cycle time
- Rework rate
- Human intervention
- Traceability
- Resource / cost efficiency

## Test Cases

อย่างน้อยควรทดสอบ:

- Happy path
- Missing input
- Invalid input
- Tool failure
- Human rejection / rework
- Re-run
- Edge case

## Evaluation Method

ใช้ PASS/FAIL เมื่อเกณฑ์ชัดเจน และใช้ตัวเลขหรือ Review เมื่อจำเป็น

ไม่สร้างคะแนนที่ดูแม่นยำหากไม่มีวิธีวัดที่น่าเชื่อถือ

## Release Gate

```text
[ ] Happy path passes
[ ] Failure paths handled
[ ] Rework path works
[ ] Output meets criteria
[ ] Dependencies traceable
[ ] Metrics captured
[ ] Known limitations recorded
```