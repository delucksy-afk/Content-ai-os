# Remediation Plan

## Priority 1 — Before Production Automation

### R-001 Runtime Integration Test

เชื่อม Tool / API จริงใน Environment ที่ควบคุมได้ และทดสอบ Success / Failure / Timeout / Retry / Duplicate

### R-002 End-to-End Contract Test

ตรวจ Payload ตั้งแต่ Brief → Research / Knowledge → Prompt → Workflow → Script → Thumbnail → Automation → Operations

### R-003 Security Review

ตรวจ Secret Storage, Permissions, External Access และ Log Redaction ก่อนใช้งานจริง

## Priority 2 — Early Production

### R-004 Operational Baseline

เก็บ Metrics ระยะเริ่มต้นเพื่อกำหนด Normal Range ของ Error, Cycle Time, Cost และ Human Intervention

### R-005 Performance Dataset

เก็บข้อมูล Content + Context + Outcome เพื่อสร้าง Learning Loop โดยไม่สรุปเหตุผลเกินข้อมูล

## Priority 3 — Optimization

### R-006 Learning Loop

เชื่อม Performance → Insight → Knowledge / Prompt / Workflow Updates

### R-007 Experiment Registry

บันทึก Hypothesis, Variant, Context, Result และ Decision เพื่อป้องกันการทดลองซ้ำโดยไม่มีความรู้สะสม
