# Automation Security Standard

**สถานะ:** ACTIVE  
**เวอร์ชัน:** v0.1

## Principles

- Least Privilege
- Secret Isolation
- Input Validation
- Output Validation
- Dependency Awareness
- Auditability
- Safe Failure

## Secrets

Credentials ต้องเก็บนอก Repository ผ่าน Secret Manager / platform secret storage ที่เหมาะสม

ห้าม:

- Commit API key
- Commit access token
- Commit password
- Put secrets in prompts, fixtures หรือ test output

## Tool Permissions

แต่ละ Automation ต้องระบุ:

- Tool / Service
- Permission required
- Data accessed
- Action performed
- Failure behavior

## External Data

ข้อมูลจาก External Service ต้องถือว่าอาจผิดพลาด ล่าช้า หรือ unavailable และควร Validate ก่อนใช้เป็น Input สำคัญ

## Incident Rule

หากสงสัยว่า Secret รั่ว:

1. หยุดการใช้งาน Credential
2. Rotate / revoke ผ่านระบบเจ้าของ Credential
3. ตรวจ Log
4. บันทึก Incident
5. ตรวจ Repository history ตามความเหมาะสม