# Thumbnail Protocol

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Standard Flow

```text
Brief / Script Handoff
 ↓
Audience & Discovery Context
 ↓
Promise Extraction
 ↓
Visual Concept
 ↓
Composition
 ↓
Text Decision
 ↓
Title Pairing
 ↓
Misleading / Accuracy Check
 ↓
Review
 ↓
Packaging Handoff
```

## Required Inputs

- Script ID / Version
- Audience
- Topic
- Core Promise
- Key Message
- Title candidate(s) when available
- Platform / placement context

## Required Outputs

- Thumbnail Concept(s)
- Visual Direction
- Text Direction / No-text decision
- Title pairing
- Risk check
- Production notes
- Version

## Missing Input Rule

หากไม่มี Script หรือ Promise ที่ชัดเจน ให้หยุดที่ `NEEDS_INPUT` หรือระบุ Assumption อย่างชัดเจน ห้ามแต่ง Promise ใหม่โดยไม่มีฐาน

## Completion Gate

```text
[ ] Script handoff validated
[ ] Audience defined
[ ] Promise defined
[ ] Visual concept clear
[ ] Title relationship checked
[ ] Misleading check passed
[ ] Production notes usable
[ ] Version recorded
```