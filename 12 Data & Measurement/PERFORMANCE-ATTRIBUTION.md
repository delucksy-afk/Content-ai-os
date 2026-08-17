# Performance Attribution Framework

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Purpose

ป้องกันการสรุปว่าองค์ประกอบหนึ่งเป็นสาเหตุของ Performance โดยไม่มีหลักฐานเพียงพอ

## Attribution Levels

### Level 0 — Observation

Metric เปลี่ยนแปลง

### Level 1 — Association

Metric มีความสัมพันธ์กับ Context / Variant

### Level 2 — Controlled Evidence

มี Experiment ที่ควบคุมตัวแปรได้เหมาะสม

### Level 3 — Repeated Evidence

ผลเกิดซ้ำใน Context ที่เหมาะสม

## Rule

ห้ามใช้ Level 0 หรือ Level 1 เป็น Causal Claim โดยอัตโนมัติ

## Context Fields

ควรพิจารณา:

- Content type
- Platform
- Audience
- Distribution context
- Time window
- Version
- Variant
- External events

## Decision

หาก Attribution ยังไม่ชัด ให้บันทึกเป็น Hypothesis / INCONCLUSIVE และออกแบบ Experiment เพิ่ม แทนการสร้างกฎถาวร