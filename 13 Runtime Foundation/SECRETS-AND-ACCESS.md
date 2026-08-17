# Secrets & Access Boundary

**สถานะ:** ACTIVE — POLICY

## Rules

1. ห้าม Commit API keys, passwords, tokens หรือ private credentials ลง Repository
2. ห้ามใส่ secrets ใน prompt logs, error logs หรือ screenshots
3. ใช้ Secret Manager / Environment Secret ของ Runtime ที่เลือกใช้จริง
4. ใช้ Least Privilege
5. แยก credentials ตาม Environment
6. Rotate / revoke เมื่อ credential รั่วหรือไม่จำเป็น
7. Access ที่เพิ่มขึ้นต้องมีเหตุผลและ scope ชัดเจน

## Permission Request Format

เมื่อระบบต้องการสิทธิ์เพิ่ม ต้องระบุ:

- Service
- Permission
- Exact purpose
- Environment
- Data accessed
- Read / Write requirement
- Risk
- Whether a narrower permission is possible

## Current Requirement

**ยังไม่ต้องส่ง credentials ให้ Repository หรือ Chat**

ก่อนเชื่อม Runtime จริง เราจะขอเฉพาะสิทธิ์ที่จำเป็นต่อ Integration ที่เลือก และควรใช้ scoped credentials / test environment ก่อน Production
