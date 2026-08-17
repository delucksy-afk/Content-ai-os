# n8n VS-001 Workflow Specification

**สถานะ:** READY FOR BUILD

## Workflow ID

`CAOS-VS001-001`

## Nodes

```text
01 Manual / Test Trigger
        ↓
02 Normalize Input
        ↓
03 Generate run_id
        ↓
04 Validate Required Fields
        ↓
05 Load Version References
        ↓
06 AI Provider Adapter
        ↓
07 Output Schema Validation
        ↓
08 Quality Gate
        ├── FAIL → Record failure → STOP
        └── PASS → Persist artifact reference
                         ↓
                    Record metric event
                         ↓
                    Return run summary
```

## Input

```text
content_id
brief
content_type
audience
platform
knowledge_version
prompt_version
workflow_version
```

## Output

```text
run_id
status
content_id
output_reference
quality_status
provider
model
versions
error_code (if failed)
```

## Quality Gate

Minimum checks:

- Required output fields exist
- No unresolved placeholder
- Output type matches requested content type
- Required policy checks pass
- No secret appears in output
- Output is linked to run_id

## Failure Behavior

Failures must return a structured status. No infinite retry.

```text
SUCCESS
REJECTED
FAILED
BLOCKED
```

## Traceability

Every successful or failed execution must be traceable to `run_id` and applicable version IDs.