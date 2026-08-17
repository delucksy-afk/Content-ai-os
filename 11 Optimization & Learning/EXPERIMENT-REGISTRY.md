# Experiment Registry

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

| ID | Objective | Baseline | Variant | Context | Status | Decision |
|---|---|---|---|---|---|---|
| — | — | — | — | — | TEMPLATE | — |

## Registry Rules

1. ทุก Experiment ที่มีผลต่อ Production ต้องมี ID
2. ต้องบันทึก Baseline ก่อนเปลี่ยน
3. ต้องบันทึก Context
4. ต้องบันทึกผลทั้ง Positive / Neutral / Negative
5. Decision ต้องอ้างอิงผลที่บันทึกไว้
6. หากผลยังไม่ชัด ให้ระบุ `INCONCLUSIVE`
7. ห้ามลบ Experiment history เพื่อให้ผลดูดีขึ้น

## Status

```text
DRAFT
READY
RUNNING
COMPLETED
INCONCLUSIVE
ADOPTED
REJECTED
ARCHIVED
```