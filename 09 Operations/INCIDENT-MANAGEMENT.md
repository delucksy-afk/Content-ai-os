# Incident Management

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Severity

### SEV-1 Critical
Security breach, severe data integrity issue, major uncontrolled output, or system-wide failure.

### SEV-2 High
Major workflow / automation failure with significant operational impact.

### SEV-3 Medium
Limited failure with workaround.

### SEV-4 Low
Minor defect or isolated issue.

## Incident Flow

```text
Detect
 ↓
Contain
 ↓
Assess
 ↓
Recover
 ↓
Verify
 ↓
Document
 ↓
Root Cause / Contributing Factors
 ↓
Prevent Recurrence
```

## Important Rule

Root Cause Analysis ไม่ควรกล่าวโทษบุคคล แต่ควรมองที่ Process, System, Dependency และ Decision ที่ทำให้เหตุการณ์เกิดขึ้นได้

## Post-Incident Review

ต้องพิจารณา:

- Detection quality
- Response time
- Failure containment
- Recovery
- Missing guardrail
- Required system change
- New test case needed