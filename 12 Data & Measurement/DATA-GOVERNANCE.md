# Data Governance

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Principles

- Collect only necessary data
- Define purpose before collection
- Minimize personal / sensitive data
- Restrict access
- Avoid unnecessary duplication in logs
- Define retention and deletion rules before implementation
- Keep audit trails for material corrections

## Data Classes

```text
PUBLIC
INTERNAL
CONFIDENTIAL
SENSITIVE
```

Classification must be determined by actual data and applicable requirements. Do not assume all production metrics are public.

## Retention

Retention period must be based on purpose, applicable requirements and operational need. No universal duration is assumed in v0.1.

## Corrections

Material corrections should preserve an audit trail rather than silently overwriting historical evidence.

## Access

Use least privilege. Access to sensitive data must be limited to the minimum necessary roles and systems.

## Logs

Prefer references and technical context over duplicating sensitive payloads in logs.