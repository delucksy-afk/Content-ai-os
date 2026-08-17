# Metrics Catalog

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Metric Definition Template

ทุก Metric ต้องมี:

- Metric ID
- Name
- Definition
- Formula / calculation method
- Source
- Unit
- Time window
- Denominator
- Context
- Owner
- Limitations
- Decision use

## Metric Families

### Production

- Content created
- Content completed
- Cycle time
- Rework rate

### Quality

- Quality pass rate
- Review rejection rate
- Critical error rate

### Distribution / Audience

ใช้เฉพาะ Metrics ที่ Platform ให้ข้อมูลและมีนิยามชัด เช่น Reach, Impressions, Click-related metrics, Watch / Retention, Engagement และ Conversion

### Operations

- Automation success rate
- Failure rate
- Retry rate
- Human intervention
- Cost per run / content

### Learning

- Experiment completion rate
- Adoption rate
- Reversion rate
- Inconclusive rate

## Metric Interpretation Rule

Metric ต้องไม่ถูกตีความนอก Context, Time Window หรือ Population ที่ใช้วัด และต้องไม่ใช้เป็น Causal proof โดยตัวมันเอง