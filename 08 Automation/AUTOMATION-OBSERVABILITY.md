# Automation Observability

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Minimum Telemetry

ทุก Run ที่เหมาะสมควรรู้:

- Run ID
- Workflow ID / Version
- Automation ID / Version
- Trigger time
- Start / End time
- State
- Input reference (ไม่เก็บ Sensitive Data โดยไม่จำเป็น)
- Output reference
- Dependency versions
- Retry count
- Error category
- Human review status

## Metrics

- Success rate
- Failure rate
- Retry rate
- Rework rate
- Cycle time
- Human intervention rate
- Cost where measurable

## Alerts

ควรมี Alert สำหรับ:

- Repeated failure
- Timeout spike
- Dependency outage
- Invalid output spike
- Unexpected cost increase
- Security incident

## Privacy

Log เฉพาะข้อมูลที่จำเป็นต่อการ Debug / Audit และหลีกเลี่ยงการเก็บ Sensitive Data โดยไม่จำเป็น