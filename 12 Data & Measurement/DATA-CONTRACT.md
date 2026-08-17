# Data Contract

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Minimum Event Schema

| Field | Required | Meaning |
|---|---|---|
| event_id | Yes | Unique event identifier |
| event_type | Yes | Type of event |
| occurred_at | Yes | Time event occurred |
| content_id | Contextual | Content identity |
| run_id | Contextual | Production run identity |
| workflow_version | Contextual | Workflow used |
| prompt_version | Contextual | Prompt used |
| knowledge_version | Contextual | Knowledge used |
| automation_version | Contextual | Automation used |
| source | Yes | Origin of data |
| value | Contextual | Measured value / payload reference |
| unit | Contextual | Unit of value |
| context | Yes | Relevant environment / platform / audience context |

## Contract Rules

- Required fields must not be silently fabricated
- Timestamps must use a consistent standard
- Units must be explicit
- Source must be identifiable
- Unknown values must be represented explicitly
- Sensitive data must not be collected unless necessary and permitted
- Schema changes require versioning

## Example Event Types

```text
CONTENT_CREATED
CONTENT_REVIEWED
CONTENT_PUBLISHED
CONTENT_METRIC_CAPTURED
AUTOMATION_STARTED
AUTOMATION_FAILED
AUTOMATION_COMPLETED
EXPERIMENT_STARTED
EXPERIMENT_COMPLETED
INCIDENT_OPENED
COST_RECORDED
```