# Automation Specification

**Automation ID:** A-YYYY-MM-DD-001  
**Version:** v0.1  
**Status:** PROTOTYPE  
**Owner:**  
**Created:** YYYY-MM-DD

## 1. Goal


## 2. Source Workflow

**Workflow ID / Version:**

## 3. Trigger

Type:

Condition:

Frequency / Event:

## 4. Inputs

| Input | Required | Validation | Sensitive? |
|---|---|---|---|
| | | | |

## 5. Dependencies

| Dependency | Version | Purpose | Failure behavior |
|---|---|---|---|
| | | | |

## 6. Execution

```text
Trigger
↓
Validate
↓
Execute
↓
Validate Output
↓
Human Gate
↓
Persist
↓
Handoff
```

## 7. State Model

```text
QUEUED → RUNNING → SUCCEEDED
             ├── WAITING_REVIEW
             ├── RETRYING
             ├── FAILED
             └── CANCELLED
```

## 8. Retry Policy

Max retries:

Backoff:

Retryable errors:

Non-retryable errors:

## 9. Idempotency

Idempotency key / strategy:

## 10. Human Review

Trigger conditions:

Reviewer action:

## 11. Security

Required permissions:

Secrets location:

Sensitive data handling:

## 12. Observability

Run ID:

Logs:

Metrics:

Alerts:

## 13. Failure / Recovery

| Failure | Detection | Action | Recovery |
|---|---|---|---|
| | | | |

## 14. Output Contract


## 15. Evaluation

```text
[ ] Functional test
[ ] Failure test
[ ] Retry test
[ ] Re-run test
[ ] Security test
[ ] Output validation
[ ] Human gate test
[ ] Observability test
```

## 16. Handoff

Next system:

Package:

## 17. Version History

| Version | Date | Change | Result |
|---|---|---|---|
| v0.1 | YYYY-MM-DD | Initial | |

## 18. Final Gate

```text
[ ] Workflow proven
[ ] Trigger defined
[ ] Inputs validated
[ ] Dependencies versioned
[ ] Retry bounded
[ ] Idempotency addressed
[ ] Failure path tested
[ ] Security passed
[ ] Human gate defined
[ ] Observability enabled
[ ] Output validated
[ ] Recovery considered
```