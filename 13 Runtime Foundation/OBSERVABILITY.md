# Observability

**สถานะ:** ACTIVE — DESIGN

## Minimum Signals

- Run started / completed / failed
- Duration
- Retry count
- Error category
- Quality gate result
- Artifact reference
- Cost event where measurable

## Logging Principles

Logs should answer:

1. What happened?
2. When?
3. Which run?
4. Which component / version?
5. What failed?
6. What action followed?

## Sensitive Data

Do not log secrets or unnecessary personal / sensitive payloads. Prefer IDs and references.

## Alerting

Alerts should be tied to actionable conditions, not every informational event.