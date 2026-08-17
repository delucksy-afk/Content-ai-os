# End-to-End Audit Matrix

| Area | What to verify | Pass condition |
|---|---|---|
| Architecture | Layer responsibilities | No major overlap / gap |
| Structure | Naming / locations | Predictable and consistent |
| Constitution | Rules / constraints | Downstream layers can comply |
| Research | Evidence capture | Sources / claims traceable |
| Knowledge | Canonical knowledge | Versioned and attributable |
| Prompt | Input / output contract | Explicit and testable |
| Workflow | Steps / decisions | Repeatable and bounded |
| Script | Production artifact | Traceable to evidence / promise |
| Thumbnail | Packaging artifact | Aligned and truthful |
| Automation | Execution controls | Validated, recoverable, observable |
| Operations | Governance | Changes / incidents / metrics controlled |
| Handoff | Boundary contracts | Required data survives transition |
| Quality | Gates | Clear PASS / FAIL / REVIEW |
| Security | Secrets / permissions | No unnecessary exposure |
| Tests | Coverage | Failure paths considered |
| Documentation | Version / changelog | Changes explainable |

## Severity

- **S0 Critical:** security / integrity / uncontrolled production risk
- **S1 High:** major system break or missing control
- **S2 Medium:** important inconsistency / maintainability risk
- **S3 Low:** documentation / polish issue

## Audit Rule

จำนวนไฟล์ไม่ใช่ตัวชี้วัดความพร้อม ระบบจะถือว่าผ่านเมื่อ Contracts, Dependencies, Handoffs และ Controls สอดคล้องกัน