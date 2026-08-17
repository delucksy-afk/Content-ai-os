# Data & Measurement Changelog

## [v0.1] — ACTIVE / DESIGN READY

**วันที่:** 2026-08-17

### Added

- Data Architecture
- Data Contract
- Metrics Catalog
- Data Quality Standard
- Data Governance
- Performance Attribution Framework
- Dataset Specification template
- D-001 Data Contract architecture test

### Decisions

- Raw data แยกจาก Derived Metrics
- Data สำคัญต้อง Trace กลับไปยัง Content / Run / Version ได้
- ห้าม silently fabricate missing data
- Metric ต้องมี Definition, Source, Context และ Limitation
- Correlation ไม่ถือเป็น Causation โดยอัตโนมัติ
- Personal / sensitive data ต้องถูกเก็บเท่าที่จำเป็น

### Status

**12 Data & Measurement v0.1 — ACTIVE / DESIGN READY**