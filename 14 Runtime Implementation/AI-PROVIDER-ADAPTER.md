# AI Provider Adapter Contract

**สถานะ:** READY FOR BUILD

## Purpose

แยก Workflow ออกจาก Vendor/Model เพื่อให้เปลี่ยน AI Provider ได้โดยไม่รื้อระบบหลัก

## Contract

### Input

```text
provider
model
system_instruction
user_input
temperature (if supported)
max_output (if supported)
```

### Output

```text
provider
model
request_id (if available)
status
text
usage (if available)
error_code
latency_ms
```

## Supported Provider Targets

- Gemini — initial candidate because user already has paid access
- OpenAI — candidate
- Claude — candidate

**Provider selection is not a claim about API entitlement. API access must be verified separately.**

## Rules

- Do not expose provider credentials to workflow outputs
- Store provider/model metadata for reproducibility
- Treat model changes as version-relevant changes
- Do not assume identical behavior across providers
- Record failures explicitly
