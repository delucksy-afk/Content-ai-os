# Automation Design Rules

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## 1. Automate Proven Work

ต้องมี Workflow ที่ชัดก่อน Automation

## 2. Explicit Contracts

Input / Output ต้องระบุรูปแบบและเงื่อนไขสำเร็จ

## 3. Least Privilege

ให้สิทธิ์ Tool / Service เท่าที่จำเป็น

## 4. No Secrets in Content

ห้ามใส่ API Keys, Tokens, Passwords หรือ Credentials ลงใน Repository

## 5. Idempotency

งานที่มีโอกาสถูก Retry ต้องออกแบบไม่ให้เกิดผลซ้ำที่เสียหาย

## 6. Bounded Retries

Retry ต้องมีจำนวนหรือเงื่อนไขสิ้นสุด ไม่วนไม่รู้จบ

## 7. Human-in-the-Loop

งานที่มีความเสี่ยงหรือ Judgment สูงต้องมี Human Gate

## 8. Fail Loudly

Failure ต้องถูกบันทึกและระบุ State ชัดเจน

## 9. Version Dependencies

Prompt, Knowledge, Workflow และ Tool configuration ที่มีผลต่อ Output ต้อง Trace ได้

## 10. Reversible Changes

การเปลี่ยน Automation สำคัญควร Rollback ได้