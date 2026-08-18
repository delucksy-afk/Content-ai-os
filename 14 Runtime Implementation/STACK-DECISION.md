# Initial Stack Decision

**Status:** DECIDED — v0.1

## Decision

`n8n` is the first Automation / Orchestration Layer for Content AI OS.

This decision applies to the first Runtime Vertical Slice (`VS-001`) and does not prohibit future evaluation of alternatives.

## Supporting Stack

| Layer | v0.1 choice | Status |
|---|---|---|
| Source of Truth | GitHub | ACTIVE |
| Orchestration | n8n | SELECTED |
| Initial AI Provider | Gemini | CANDIDATE / TEST |
| Artifact Storage | Google Drive | TEST PLANNED |
| V1 Operational Data | Google Sheets | TEST PLANNED |
| Public Web Layer | gmterminal.today | APPROVED FOR MIGRATION |

## Evaluation Criteria

| Criterion | Weight | Question |
|---|---:|---|
| Integration fit | High | เชื่อม Workflow / AI / Storage ได้หรือไม่ |
| Observability | High | ตรวจ Run / Error / Cost ได้หรือไม่ |
| Versionability | High | เปลี่ยนและย้อน Version ได้หรือไม่ |
| Security | High | Secret / Permission ควบคุมได้หรือไม่ |
| Reliability | High | Retry / Timeout / Failure control ดีหรือไม่ |
| Cost | Medium | เหมาะกับระยะทดลองหรือไม่ |
| Portability | Medium | ย้ายออกได้หรือไม่ |
| Simplicity | High | ดูแลคนเดียวได้หรือไม่ |

## Decision Rule

เลือก Stack ที่ทำให้ Vertical Slice `VS-001` ผ่านได้ด้วยความซับซ้อนต่ำที่สุด โดยไม่ลด Security, Traceability หรือ Quality Controls

## Important Boundary

`gmterminal.today` เป็น Public Web / User Interface ไม่ใช่ Source of Truth และไม่ควรเก็บ secrets หรือ workflow definitions สำคัญไว้ใน frontend

## Current Gate

n8n = **SELECTED**  
Gemini = **TEST CANDIDATE**  
Google Drive / Sheets = **TEST PLANNED**  
`gmterminal.today` = **APPROVED FOR DIRECT MIGRATION — DNS/HOSTING CUTOVER PENDING**
