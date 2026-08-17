# Optimization Metrics Framework

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Metric Families

### Quality

- Quality pass rate
- Rework rate
- Human rejection rate
- Critical error rate

### Audience / Content Performance

ใช้ Metrics ที่เหมาะกับ Platform และ Content เช่น:

- Reach / impressions
- Click / click-through metrics
- Watch / retention metrics
- Engagement metrics
- Conversion metrics where applicable

ไม่ควรตีความ Metric ใดโดยไม่ดู Context และ denominator ที่เกี่ยวข้อง

### Operational

- Cycle time
- Failure rate
- Retry rate
- Human intervention
- Cost

### Learning

- Experiments completed
- Decision rate
- Adoption rate
- Reverted changes
- Inconclusive rate

## Metric Discipline

ทุก Metric ควรระบุ:

- Definition
- Source
- Time window
- Context
- Denominator
- Known limitations

## Anti-Pattern

ห้ามทำ Dashboard ที่รวมตัวเลขจำนวนมากโดยไม่มี Decision ที่ตัวเลขเหล่านั้นใช้สนับสนุน