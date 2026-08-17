# Prompt Test — P-001

**Prompt ID:** P-2026-08-17-001  
**Version:** v0.1  
**Status:** TESTED  
**Knowledge:** K-2026-08-17-001

## Objective

สร้างแนวทางเสนอ Title + Thumbnail concepts สำหรับ YouTube โดยใช้ Knowledge ที่ผ่านการตรวจสอบ และไม่สัญญาผลลัพธ์ด้าน CTR แบบตายตัว

## Input Contract

- Topic
- Target audience
- Video promise
- Tone

หากข้อมูลสำคัญหายไป ให้ระบุสิ่งที่ขาดแทนการเดา

## Knowledge Dependency

`K-2026-08-17-001`

## Instructions

1. วิเคราะห์ Topic และ Audience
2. เสนอ Title concepts ที่แตกต่างกันตาม Searchable / Intriguing intent เมื่อเหมาะสม
3. เสนอ Thumbnail concepts ที่เสริม Title ไม่ใช่ทำซ้ำข้อความทั้งหมด
4. ตรวจว่า Promise สอดคล้องกับเนื้อหาที่ให้มา
5. ห้ามอ้างว่าแนวคิดใดรับประกัน CTR สูง
6. ระบุเหตุผลสั้น ๆ ต่อแนวคิด

## Constraints

- ไม่ใช้ Clickbait ที่ทำให้ผู้ชมคาดหวังสิ่งที่วิดีโอไม่มี
- ไม่สร้างข้อมูลเกี่ยวกับวิดีโอที่ไม่ได้รับจาก Input
- หาก Context ไม่พอให้ถาม / ระบุข้อมูลที่ขาด

## Output Contract

```text
1. Audience / Intent
2. Title Concepts — 5 options
3. Thumbnail Concepts — 5 options
4. Pairing Recommendation — 3 pairs
5. Risk / Misleading Check
6. Missing Information
```

## Quality Criteria

- Relevant
- Clear
- Non-misleading
- Knowledge-aligned
- Output format complete
- No guaranteed-performance claim

## Test Cases

### Normal
มี Topic, Audience, Promise ครบ → สร้าง Output ได้

### Missing
ไม่มี Target Audience → ต้องระบุ Missing Information และไม่เดา

### Ambiguous
Topic กว้างมาก → ต้องชี้ Assumption หรือขอ Context เพิ่ม

## Evaluation

**Status:** PASS

เหตุผล: Prompt มี Objective, Input Contract, Knowledge Dependency, Instructions, Constraints, Output Contract, Quality Criteria และ Failure Behavior ครบตาม Prompt Protocol

## Limitations

ยังเป็น Architecture Test ไม่ใช่การวัด Performance กับข้อมูลจำนวนมากหรือหลาย Model

## Next

เมื่อใช้จริงให้เก็บ Failure Cases และปรับ Prompt เป็น Version ถัดไป