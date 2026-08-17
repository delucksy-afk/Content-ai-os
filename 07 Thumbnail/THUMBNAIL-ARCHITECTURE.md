# Thumbnail Architecture

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Layers

```text
L1 Content Context
L2 Audience / Discovery Context
L3 Core Promise
L4 Visual Angle
L5 Composition
L6 Text / No-text
L7 Title Relationship
L8 Accuracy / Misleading Check
L9 Production Specification
L10 Evaluation
```

## Packaging Relationship

```text
        Content Promise
             │
       ┌─────┴─────┐
       ▼           ▼
     Title     Thumbnail
       │           │
       └─────┬─────┘
             ▼
          Content
```

ทั้งสามส่วนต้องทำงานไปในทิศทางเดียวกัน แต่ไม่จำเป็นต้องสื่อสารข้อความเดียวกันทุกคำ

## Separation of Concerns

Thumbnail บอก Visual Promise / Cue

Title บอก Topic / Promise ด้วยภาษาของข้อความ

Script ส่งมอบ Value จริง

## Output

ผลลัพธ์ของระบบคือ `Thumbnail Brief / Production Specification` ไม่ใช่การรับประกัน Performance