# Runtime Access Request

**สถานะ:** REQUEST READY — DO NOT SHARE SECRETS IN CHAT

## Principle

ขอสิทธิ์แบบ Least Privilege และเริ่มจาก TEST / DEV ก่อน Production เสมอ

## Required for VS-001

### 1. n8n

- Environment: DEV / TEST
- Permission: Create / Edit / Execute workflow
- Purpose: Build and run VS-001
- Credential storage: Required
- Production access: Not requested

### 2. Gemini API — Initial Provider Candidate

- Environment: TEST
- Permission: API invocation only
- Purpose: AI generation in VS-001
- Credential: Must be stored in the provider / n8n credential store
- Do not paste API key into chat or GitHub

### 3. Google Drive

- Environment: TEST
- Permission: Access only to a dedicated test folder where possible
- Purpose: Store VS-001 output artifacts
- Production Drive: Not requested

### 4. Google Sheets

- Environment: TEST
- Permission: Access only to a dedicated test spreadsheet where possible
- Purpose: Store run / measurement records
- Production Sheets: Not requested

## Not Requested Yet

- YouTube publishing permission
- Production Google Drive access
- Production Sheets data
- OpenAI API
- Claude API
- GitHub administrative permission

## Security Rule

Never send raw API keys, passwords, tokens or other secrets in chat. Enter credentials only into the relevant secure credential store.

## Next Action

User should first prepare a TEST n8n environment. No credential values need to be shared with the assistant.