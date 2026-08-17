# Workflow Specification

**Workflow ID:** W-YYYY-MM-DD-001  
**Version:** v0.1  
**Status:** DRAFT  
**Owner:**  
**Created:** YYYY-MM-DD

## 1. Goal


## 2. Trigger


## 3. Inputs

Required:

- 

Optional:

- 

Missing input behavior:

- 

## 4. Dependencies

### Knowledge

- ID / Version:

### Prompts

- ID / Version:

### Tools

- 

## 5. Workflow Stages

| # | Stage | Input | Action | Actor/Tool | Output | Success Criteria |
|---|---|---|---|---|---|---|
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |

## 6. Decision Gates

### Gate 1

Condition:

Pass:

Fail / Rework:

## 7. State Model

```text
NEW → IN_PROGRESS → REVIEW → APPROVED → COMPLETE
                         ↘ REWORK
```

## 8. Failure / Exception Paths

| Failure | Detection | Response | Owner |
|---|---|---|---|
| | | | |

## 9. Human Review

เมื่อใดต้องให้มนุษย์ตรวจ:

- 

## 10. Output Contract


## 11. Handoff

ส่งต่อให้:

- 

เงื่อนไขพร้อมส่งต่อ:

- 

## 12. Metrics

- Completion rate:
- Failure rate:
- Rework rate:
- Cycle time:
- Human intervention:

## 13. Test Cases

- Happy path:
- Missing input:
- Invalid input:
- Tool failure:
- Rework:
- Re-run:
- Edge case:

## 14. Version History

| Version | Date | Change | Result |
|---|---|---|---|
| v0.1 | YYYY-MM-DD | Initial | |

## 15. Final Gate

```text
[ ] Goal clear
[ ] Trigger defined
[ ] Inputs defined
[ ] Dependencies versioned
[ ] Stages complete
[ ] Decision gates defined
[ ] Failure paths defined
[ ] Human review defined
[ ] Output contract defined
[ ] Handoff defined
[ ] Metrics defined
[ ] Tests passed
```