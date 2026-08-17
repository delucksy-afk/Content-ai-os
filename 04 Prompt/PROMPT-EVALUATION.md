# Prompt Evaluation

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Purpose

ประเมิน Output จริงของ Prompt แทนการตัดสินจากความรู้สึกว่า Prompt ดูดี

## Evaluation Dimensions

- Task Success
- Accuracy
- Instruction Following
- Relevance
- Completeness
- Consistency
- Format Compliance
- Safety / Policy Compliance when applicable

## Evaluation Types

### Rule-based
ตรวจตามเงื่อนไขที่กำหนดได้ชัดเจน

### Example-based
เปรียบเทียบกับ Expected Characteristics หรือ Reference Output

### Human Review
ใช้เมื่อคุณภาพต้องอาศัย Judgment หรือความเสี่ยงสูง

## Test Set

Prompt สำคัญควรมี Test Cases ที่ครอบคลุม:

- Normal Input
- Edge Case
- Ambiguous Input
- Missing Input
- Adversarial / conflicting instruction when relevant

## Scoring

ใช้คะแนนเท่าที่มีประโยชน์ ไม่ใช้ตัวเลขเพื่อสร้างความแม่นยำปลอม

ตัวอย่าง:

```text
PASS / FAIL
```

หรือ

```text
1–5 + เหตุผล
```

## Release Gate

```text
[ ] Test set exists
[ ] Critical failures addressed
[ ] Quality criteria passed
[ ] Known limitations recorded
[ ] Version recorded
```