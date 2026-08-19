# Artefact Health Check Summary (Baseline Review v1.0)

> **Case:** Classroom & Laboratory Maintenance Reporting System (Case No.02)
> **Date:** 19 สิงหาคม 2569
> **Evaluator:** Scribe & Facilitator (Group 02)

## 1. Audit Table

| เอกสาร / โฟลเดอร์ | ต้องมีอะไรอยู่ข้างใน | สถานะการตรวจ | หมายเหตุ / จุดที่ตรวจพบ |
|---|---|---|---|
| `docs/01-problem-brief-v0.1.md` | Problem statement, Facts, Pain points, Stakeholder เริ่มต้น, Scope เบื้องต้น, NFR เริ่มต้น | **[x] ครบ** | แยก Facts (F-01..F-05), Pain Points (PP-01..PP-05) และ Initial User Needs (UN-01..UN-04) ชัดเจน |
| `docs/02-stakeholder-context-scope.md` | Stakeholder map/profiles, System context, Data flow, In/Out scope, Constraints, Privacy & Ethics | **[x] ครบ** | มี Stakeholder Profile ครบ 4 กลุ่ม, Data Flow table, Scope statement และ Privacy/Ethics/Responsible AI section |
| `docs/03-elicitation-plan.md` | Objectives, Elicitation plan ต่อ Stakeholder, Technique rationale, Readiness check | **[x] ครบ** | มีแผนสัมภาษณ์ EP-01..EP-05 ตาม Stakeholder แต่ละกลุ่ม พร้อม Risk & Mitigation |
| `docs/04-evidence-log.md` | Evidence ติด Tag, Traceability gap, Need Summary, Open Questions | **[x] ครบ** | มี E-01..E-07 พร้อม Tag/Related RC ครบ, RC-F-05 Traceability Gap ถูกบันทึกไว้อย่างชัดเจน (v0.4 เพิ่ม Downstream Traceability Audit) |
| `docs/04-negotiation-record.md` | Position/Interest, Decision (Provisional/Unresolved), Derived RC | **[x] ครบ** | N-01..N-03 มี E-ID อ้างอิง ตัวเลือก > 2 และระบุ Next Owner สำหรับข้อ Unresolved |
| `docs/04-requirement-candidates.md` | Evidence → Need → RC, RC table, เหตุผลที่ยังไม่ Final, Week05 handoff | **[x] ครบ** | RC-F-01..RC-F-08 อ้าง Evidence E-ID ครบ ยกเว้น RC-F-05 ที่บันทึกเป็น Gap โดยตั้งใจ |
| `docs/05-requirement-backlog.md` | FR/NFR + Source RC + Priority + Acceptance Measure | **[△] ครบแต่พบข้อผิดพลาด** | **พบ RC-F-05 และ RC-F-06 ถูกอ้างสลับความหมายกับ `04-requirement-candidates.md`** — FR-CLMRS-05 (Source RC-F-05) เป็นเรื่องแจ้งซ้ำ แต่ candidates.md ให้ RC-F-05 = ปิดงาน (ดูรายละเอียดใน `peer-cross-review.md` ข้อ 1) |
| `docs/05-open-questions-and-issues.md` | Open Questions + Related Evidence/RC, Issues/Holds, Follow-up Plan | **[△] ครบแต่พบการอ้างอิงคลาดเคลื่อน** | OQ-01 อ้าง Related Evidence เป็น `E-04` (ที่จริงคือเรื่องแจ้งซ้ำ ไม่ใช่ Urgent — ควรเป็น E-02) และ OQ-03 อ้างรหัส `CU-01` ที่ไม่ปรากฏใน Evidence Log |
| `docs/05-prioritization-rationale.md` | MoSCoW rationale ต่อ Requirement, สิ่งที่ยังไม่เลือกเป็น Requirement | **[x] ครบ** | Req ID และ Priority ตรงกับ `05-requirement-backlog.md` v0.2 ทุกแถว |
| `docs/06-requirement-models.md` | User Story, Use Case, Acceptance Criteria, Diagram links | **[ ] ยังไม่ครบ** | ยังเป็น Template ว่างทั้งหมด ([กรอก]) — ยังไม่เริ่มทำ Week06 |
| `docs/07-srs-v1.md` | SRS section 1-9 ครบตาม IEEE-style outline | **[ ] ยังไม่ครบ** | ยังเป็น Template ว่างทั้งหมด ([กรอก]) — รอ Backlog นิ่งก่อนจึงเริ่ม Baseline ได้ |
| `docs/08-validation-traceability.md` | Validation Plan, Quality Checklist, Traceability Matrix, Change Log | **[ ] ยังไม่ครบ** | ยังเป็น Template ว่างทั้งหมด ([กรอก]) — ยังไม่มี Traceability Matrix ฉบับเต็มรองรับ |

**สรุปสถานะ:** 9 จาก 12 เอกสาร **ครบ**, 2 เอกสาร **ครบแต่พบข้อผิดพลาดด้านการอ้างอิง (ต้องแก้ก่อน Week06)**, 3 เอกสาร **ยังไม่เริ่ม (Template ว่าง — ตามกำหนดการของ Week06-08)**

---

## 2. Summary & Self-Check Findings

1. **เอกสารช่วงไหนที่ทีม "ครบน้อยที่สุด"?**
   - `docs/06-requirement-models.md`, `docs/07-srs-v1.md` และ `docs/08-validation-traceability.md` ยังเป็น Template ว่างทั้งหมด เนื่องจากยังไม่ถึงกำหนดส่งงาน (Week06-08) — ไม่ถือเป็นข้อผิดพลาด แต่เป็นงานที่ต้องเริ่มทำหลังจาก Backlog นิ่ง

2. **มีข้อผิดพลาดด้าน Traceability ที่พบระหว่างการตรวจหรือไม่?**
   - พบ 2 จุด: (1) `05-requirement-backlog.md` ใช้ RC-F-05/RC-F-06 สลับความหมายกับต้นทางใน `04-requirement-candidates.md` (2) `05-open-questions-and-issues.md` อ้าง Evidence ID ผิดใน OQ-01 และอ้างรหัสที่ไม่มีอยู่จริง (`CU-01`) ใน OQ-03 — รายละเอียดเต็มอยู่ใน `peer-cross-review.md`

3. **มีหัวข้อใดที่เคยข้ามไปตอนทำจริงไหม?**
   - ไม่มีหัวข้อที่ข้าม เอกสาร Week01-05 มีเนื้อหาครบตามแบบฟอร์มมาตรฐานของรายวิชา ENGSE206 ปัญหาที่พบเป็นเรื่องความสอดคล้องของรหัสอ้างอิง (Reference ID) ระหว่างไฟล์ ไม่ใช่เนื้อหาที่ขาดหาย

4. **Next Action ก่อน Baseline v1.0:**
   - แก้ไข RC-F-05/RC-F-06 ใน `05-requirement-backlog.md` ให้ตรงกับ `04-requirement-candidates.md`
   - แก้ไข Related Evidence/RC ใน `05-open-questions-and-issues.md` (OQ-01, OQ-03) ให้ตรงกับ `04-evidence-log.md`
   - เริ่มดำเนินการ `06-requirement-models.md` ต่อจาก Requirement ที่มีสถานะ "Ready for Week06" (FR-CLMRS-01, FR-CLMRS-04)