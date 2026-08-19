# ใบตรวจข้ามทีม (Peer Cross-Review Form) — Baseline Review v1.0

> **Case Project:** Classroom & Laboratory Maintenance Reporting System (Case No.02)
> **Review Date:** 19 สิงหาคม 2569
> **Reviewing Sub-team / Peer Group:** Internal Baseline Review (Group 02)
> **Target Artefacts Reviewed:** `docs/04-evidence-log.md`, `docs/04-requirement-candidates.md`, `docs/05-requirement-backlog.md`, `docs/05-open-questions-and-issues.md`

---

## 1. ผลการตรวจข้ามทีม (Checklist Evaluation)

| # | สิ่งที่ตรวจ | ผลการประเมิน (ผ่าน / ไม่ผ่าน) | ข้อเสนอแนะ / หมายเหตุ (อ้าง ID เสมอ) |
|---|---|---|---|
| 1 | **ทุก Must มีสาย traceable ครบ** (Evidence → Need → RC → FR/NFR) | [ ] ผ่าน **[x] ไม่ผ่าน** | FR-CLMRS-01, FR-CLMRS-02, FR-CLMRS-04, NFR-CLMRS-01 (Must) มีสาย Traceability ครบ แต่ **RC-F-05 กับ RC-F-06 ถูกอ้างสลับความหมายกันระหว่าง `04-requirement-candidates.md` กับ `05-requirement-backlog.md`** — ใน candidates.md RC-F-05 = ปิดงาน (ไม่มี Evidence) และ RC-F-06 = แจ้งซ้ำ (E-04) แต่ backlog กลับให้ FR-CLMRS-05 (Source RC-F-05) เป็นเรื่องแจ้งซ้ำ (trace E-04→N-04) และ FR-CLMRS-06 (Source RC-F-06) เป็นเรื่องปิดงาน (trace OQ-02→N-02) ทำให้สายอ้างอิงของทั้งสองข้อชี้ผิดทาง |
| 2 | **Evidence citation ถูกต้องตรงกับ Evidence Log** | [ ] ผ่าน **[x] ไม่ผ่าน** | `05-open-questions-and-issues.md` OQ-01 อ้าง Related Evidence เป็น `E-04` แต่ E-04 ใน `04-evidence-log.md` คือเรื่องแจ้งปัญหาซ้ำ ไม่ใช่เรื่องความเร่งด่วน (Urgent มาจาก E-02) และ OQ-03 อ้างรหัส `CU-01` ซึ่งไม่ปรากฏใน Evidence Log ที่ใดเลย |
| 3 | **FR/NFR วัด/ทดสอบได้** (มี Acceptance Measure เชิงปริมาณ ชัดเจน) | **[x] ผ่าน** [ ] ไม่ผ่าน | ทุกแถวใน `05-requirement-backlog.md` v0.2 มี Acceptance Measure ระบุไว้ครบ เช่น FR-CLMRS-01 (ได้เลขที่อ้างอิงทันทีหลังส่ง), FR-CLMRS-02 (ระบบปฏิเสธคำขอหากฟิลด์บังคับไม่ครบ) |
| 4 | **ไม่มี requirement กำกวม/ซ้ำ** (Atomic & Unambiguous) | **[x] ผ่าน** [ ] ไม่ผ่าน | ถ้อยคำแยก Atomic ชัดเจนระหว่างการแจ้งปัญหา (FR-CLMRS-01), การบันทึกข้อมูลขั้นต่ำ (FR-CLMRS-02), การจัดลำดับความเร่งด่วน (FR-CLMRS-03) และการติดตามสถานะ (FR-CLMRS-04) — ไม่มีข้อความซ้ำซ้อนกัน |
| 5 | **Scope ตรงกับ Case Card** (ไม่บวมเกินขอบเขตที่ได้รับมอบหมาย) | **[x] ผ่าน** [ ] ไม่ผ่าน | ขอบเขตสอดคล้องกับ Case No.02 ระบบแจ้งซ่อมอุปกรณ์ห้องเรียน/ห้องปฏิบัติการ และระบุ Out-of-scope ชัดเจนใน `02-stakeholder-context-scope.md` (เช่น ไม่รวมระบบจัดซื้อ งบประมาณ หรือควบคุมอาคารอัตโนมัติ) |
| 6 | **MoSCoW มีเหตุผลรองรับ** (Rationale สมเหตุสมผลจาก Value/Risk/Urgency/Dependency) | **[x] ผ่าน** [ ] ไม่ผ่าน | `05-prioritization-rationale.md` ให้เหตุผลราย Requirement ครบ และ Req ID/Priority ตรงกับ `05-requirement-backlog.md` ทุกแถวตามที่ระบุไว้ใน Review Checklist ของ backlog เอง |
| 7 | **Unresolved/Needs Validation ไม่ถูกยกระดับเป็น Requirement มั่นคงโดยไม่มีหลักฐาน** | **[x] ผ่าน** [ ] ไม่ผ่าน | RC-F-05 ถูกบันทึกเป็น "Needs Validation" พร้อม Traceability Gap อย่างชัดเจนใน `04-evidence-log.md` Section 3 แทนที่จะสร้าง Evidence ขึ้นมาเอง ถือเป็นแนวปฏิบัติที่ถูกต้อง |

**ผลรวม: 5 ผ่าน / 2 ไม่ผ่าน (จาก 7 ข้อ)**

---

## 2. ข้อเสนอแนะเพื่อการปรับปรุงและเตรียมพร้อม Week 06 (Constructive Feedback)

1. **ด้าน Traceability (อ้างอิง RC-F-05, RC-F-06, FR-CLMRS-05, FR-CLMRS-06):**
   - ต้องเลือกยึดไฟล์ใดไฟล์หนึ่งเป็น Single Source of Truth สำหรับความหมายของ RC-ID แนะนำให้ยึด `04-requirement-candidates.md` (ต้นทางจาก Evidence Log) เป็นหลัก แล้วแก้ `05-requirement-backlog.md` ให้ Source RC ตรงกัน: FR-CLMRS-05 (แจ้งซ้ำ) ควรอ้าง RC-F-06 และ FR-CLMRS-06 (ปิดงาน) ควรอ้าง RC-F-05

2. **ด้าน Evidence Citation Accuracy (อ้างอิง OQ-01, OQ-03):**
   - แก้ `05-open-questions-and-issues.md` ให้ OQ-01 อ้าง E-02 แทน E-04 และตรวจสอบว่า `CU-01` ใน OQ-03 หมายถึงอะไร หากไม่มีอยู่จริงควรลบออกหรือแทนที่ด้วย E-04/RC-F-06 ให้ตรงกับ Evidence Log

3. **ด้านการเตรียมต่อยอดสู่ Requirement Modeling (Week 06 Handoff):**
   - แนะนำให้เริ่มจาก FR-CLMRS-01 และ FR-CLMRS-04 (สถานะ "Ready for Week06") ไปทำ User Story และ Use Case ก่อน เนื่องจากไม่มีปัญหา Traceability และมี Acceptance Measure ชัดเจนแล้ว ส่วน FR-CLMRS-05/06 ควรรอจนกว่าจะแก้ไขปัญหาข้อ 1 เสร็จก่อนจึงเริ่มทำ Model

---

## 3. สรุปผลการประเมิน (Gate Assessment Result)

- **สถานะ:** **ผ่านแบบมีเงื่อนไข (PASS WITH CONDITIONS)** — ผ่าน 5/7 ข้อ พบ 2 ข้อที่ต้องแก้ไขก่อนประกาศ Baseline v1.0 อย่างเป็นทางการ
- **เงื่อนไขที่ต้องแก้ก่อนปิด Gate:**
  1. แก้ไขการอ้าง RC-F-05/RC-F-06 ใน `05-requirement-backlog.md` ให้ตรงกับ `04-requirement-candidates.md`
  2. แก้ไข Related Evidence ใน `05-open-questions-and-issues.md` (OQ-01, OQ-03) ให้ตรงกับ `04-evidence-log.md`
- **ผู้ตรวจสอบ (Cross-Reviewers):** นายสันติ ปัญญาหน้อย, นายธีรนัย ไชยกันทะ, นายบูรพา ประทีปรัตน์
- **วันที่ยืนยันผล:** 19 สิงหาคม 2569