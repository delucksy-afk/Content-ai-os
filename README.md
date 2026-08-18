# Content AI OS

ระบบต้นแบบสำหรับออกแบบและสร้าง Content AI Operating System แบบตรวจสอบย้อนกลับได้

## Source of Truth

GitHub Repository นี้เป็น Source of Truth สำหรับ Architecture, Constitution, Policies, Contracts, Workflow Specifications, Runtime Design และ Evidence

## Current Architecture

```text
00 Project Overview
 ↓
01 Constitution
 ↓
02 Research
 ↓
03 Knowledge
 ↓
04 Prompt
 ↓
05 Workflow
 ↓
06 Script
 ↓
07 Thumbnail
 ↓
08 Automation
 ↓
09 Operations
 ↓
10 Full System Audit
 ↓
11 Optimization & Learning
 ↓
12 Data & Measurement
 ↓
13 Runtime Foundation
 ↓
14 Runtime Implementation
 ↓
15 Public Web Layer
```

## Current Runtime Decision

- Orchestration: **n8n**
- Initial AI Provider candidate: **Gemini**
- Artifact storage candidate: **Google Drive**
- V1 operational data candidate: **Google Sheets**
- Public Web domain: **gmterminal.today** — migration planned, DNS not changed yet

## Important Boundaries

- Secrets never belong in Git
- Production access is not required for the first Runtime Slice
- `VS-001` must have real execution evidence before being marked PASS
- Public Web is an interface, not the system's Source of Truth
