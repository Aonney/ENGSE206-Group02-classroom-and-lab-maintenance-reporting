# 08 — Validation, Traceability and Change Management

> **Week 8 deliverable**
>
> **Project:** Classroom & Laboratory Maintenance Reporting System (CLMRS)
>
> **Case:** ระบบแจ้งซ่อมอุปกรณ์ในห้องเรียนและห้องปฏิบัติการ
>
> **Team:** Group 02

---

# 1. Validation Plan

| Validation Activity | Artefact | Participants | Criteria | Evidence |
|---|---|---|---|---|
| Peer Review / Stakeholder Simulation / Checklist | docs/01 ถึง docs/05 และ SRS v1 | นักศึกษา, อาจารย์ผู้สอน, ตัวแทนผู้ใช้งาน/เจ้าหน้าที่ | completeness, consistency, feasibility, testability, traceability, scope alignment, MoSCoW rationale | `../evidence/week-08/` |

---

# 2. Requirements Quality Checklist

| Check | Result | Evidence / Note |
|---|---|---|
| Requirement มี ID และไม่ซ้ำกัน | Pass | FR-CLMRS-01 ถึง FR-CLMRS-09 และ NFR-CLMRS-01 มี ID แยกกัน |
| ใช้ถ้อยคำชัดเจน ไม่กำกวม | Pass | ใช้คำว่า "ระบบต้อง..." หรือ "ระบบควร..." และระบุพฤติกรรมที่ระบบต้องรองรับ |
| ตรวจรับหรือวัดผลได้ | Pass | Requirement สามารถนำไปสร้าง Use Case, Acceptance Criteria และ Test Case ได้ |
| มี source/rationale | Pass | Requirement เชื่อมโยงกับ Evidence, Need และ Requirement Candidate |
| Scope เหมาะสม | Pass | ครอบคลุมการแจ้งปัญหา การเก็บข้อมูล การจัดลำดับความเร่งด่วน การติดตามสถานะ การจัดการปัญหาซ้ำ และการส่งต่องาน |

---

# 3. Traceability Matrix

| Stakeholder Need | FR / NFR | User Story / Use Case | Design Element | Verification / Review |
|---|---|---|---|---|
| UN-01 ผู้ใช้งานต้องการช่องทางมาตรฐานในการแจ้งปัญหา | FR-CLMRS-01 | US-01 / UC-01 แจ้งปัญหา | Report Issue Screen | Functional Review |
| UN-02 ผู้ใช้งานต้องการให้ข้อมูลการแจ้งปัญหาครบถ้วน | FR-CLMRS-02 | US-02 / UC-01 แจ้งปัญหา | Report Form | Acceptance Criteria |
| UN-03 อาจารย์และเจ้าหน้าที่ต้องสามารถจัดลำดับงานเร่งด่วน | FR-CLMRS-03 | US-03 / UC-02 จัดลำดับความเร่งด่วน | Priority / Urgent Component | Scenario Review |
| UN-04 ผู้แจ้งต้องสามารถติดตามสถานะงานซ่อม | FR-CLMRS-04 | US-04 / UC-03 ติดตามสถานะ | Issue Tracking Screen | Functional Review |
| UN-05 เจ้าหน้าที่ต้องสามารถตรวจสอบปัญหาที่แจ้งซ้ำ | FR-CLMRS-05 | US-05 / UC-04 จัดการรายการแจ้งซ้ำ | Duplicate Issue Component | Alternate Flow Review |
| UN-06 เจ้าหน้าที่ต้องสามารถบันทึกผลและปิดงานซ่อม | FR-CLMRS-06 | US-06 / UC-05 ปิดงานซ่อม | Maintenance Management Screen | Workflow Review |
| UN-07 เจ้าหน้าที่ต้องติดตามงานที่ส่งต่อระหว่างหน่วยงาน | FR-CLMRS-07 | US-07 / UC-06 ส่งต่องาน | Assignment / Transfer Component | Workflow Review |
| UN-08 ผู้ใช้งานต้องได้รับข้อมูลเมื่อสถานะงานเปลี่ยนแปลง | FR-CLMRS-08 | US-08 / UC-03 ติดตามสถานะ | Status Update / Notification Component | Event Review |
| UN-09 ผู้บริหารต้องดูข้อมูลภาพรวมของงานซ่อมได้ | FR-CLMRS-09 | US-09 / UC-07 รายงานงานซ่อม | Maintenance Dashboard / Report | Report Review |
| UN-10 ระบบต้องควบคุมสิทธิ์ตามบทบาท | NFR-CLMRS-01 | US-10 / UC-08 Access Control | Role-based Access Control | Security Review |

> **หมายเหตุ:** การแจ้งเตือนผ่าน LINE ยังไม่ถูกกำหนดเป็น Requirement เนื่องจาก OQ-04 ยังไม่ได้ยืนยันช่องทางการแจ้งเตือนที่เหมาะสม

---

# 4. Traceability Exceptions / Open Questions

| ID | Requirement | Gap / Unknown | Action |
|---|---|---|---|
| OQ-01 | FR-CLMRS-03 | ยังไม่ยืนยันเกณฑ์ที่ใช้กำหนดงาน Urgent | สอบถามอาจารย์ผู้สอน/เจ้าหน้าที่ |
| OQ-02 | FR-CLMRS-06 | ยังไม่ยืนยันว่าใครเป็นผู้รับผิดชอบและผู้ยืนยันการปิดงาน | ตรวจสอบ Workflow กับผู้เกี่ยวข้อง |
| OQ-03 | FR-CLMRS-05 | ยังไม่ยืนยันว่ารายการแจ้งปัญหาซ้ำควรรวม เชื่อม หรือปิดรายการใด | สอบถามเจ้าหน้าที่ผู้รับผิดชอบ |
| OQ-04 | FR-CLMRS-08 | ยังไม่ยืนยันช่องทางและเงื่อนไขการแจ้งเตือน | สอบถามผู้ใช้งานและเจ้าหน้าที่ |
| OQ-05 | FR-CLMRS-09 | ยังไม่ยืนยันว่าผู้บริหารต้องการรายงานหรือสถิติใด | สอบถามผู้บริหาร/ผู้ดูแลอาคาร |
| OQ-06 | FR-CLMRS-07 | ยังไม่ยืนยันผู้รับผิดชอบหลักหลังส่งต่องาน | ตรวจสอบ Workflow ระหว่างหน่วยงาน |

---

# 5. Change Request Log

| CR-ID | Date | Requested Change | Reason / Evidence | Impacted Artefacts | Decision | Owner |
|---|---|---|---|---|---|---|
| CR-01 | 18/08/2026 | ปรับ Requirement Candidate RC-F-01 ถึง RC-F-07 ให้สอดคล้องกับ Evidence และ Need Summary | ผลจากการตรวจสอบ Traceability ระหว่าง Evidence → Need → Requirement | docs/04-evidence-log.md, docs/04-requirement-candidates.md, docs/05-requirement-backlog.md | Accepted | Project Team |
| CR-02 | 18/08/2026 | เพิ่ม Requirement สำหรับการจัดการปัญหาที่มีการแจ้งซ้ำ | พบ Open Question OQ-03 และ Need N-04 เกี่ยวกับปัญหาซ้ำ | docs/05-requirement-backlog.md, docs/08-validation-traceability.md | Accepted | Project Team |
| CR-03 | 18/08/2026 | ปรับ Requirement เรื่อง Urgent ให้เป็น Needs Follow-up | ยังไม่มีเกณฑ์ที่ยืนยันได้สำหรับการกำหนดงาน Urgent | docs/05-requirement-backlog.md | Accepted | Project Team |
| CR-04 | 18/08/2026 | ไม่กำหนด LINE Notification เป็น Requirement | OQ-04 ยังไม่ยืนยันช่องทางการแจ้งเตือน | docs/05-requirement-backlog.md, docs/08-validation-traceability.md | Accepted | Project Team |
| CR-05 | 18/08/2026 | ตรวจสอบ Requirement ที่เกี่ยวข้องกับการปิดงานและการส่งต่องาน | ต้องยืนยันผู้รับผิดชอบและ Workflow ก่อนจัดทำ Use Case | docs/05-requirement-backlog.md, docs/08-validation-traceability.md | Needs Follow-up | Project Team |

---

# 6. Baseline Decision

- **Baseline name:** `srs-v1.0`
- **Date:** 18/08/2026
- **Approved/Reviewed by:** Project Team
- **Status:** Draft Baseline
- **Remaining open issues:** OQ-01 ถึง OQ-06

### Baseline Decision

Requirement ที่มี Evidence รองรับชัดเจนสามารถนำไปใช้ต่อใน Design และ Week 06 ได้

ส่วน Requirement ที่ยังมี Open Question เช่น

- เกณฑ์งาน Urgent
- ผู้ยืนยันการปิดงาน
- วิธีจัดการปัญหาที่แจ้งซ้ำ
- ช่องทางการแจ้งเตือน
- รูปแบบรายงานของผู้บริหาร
- Workflow การส่งต่องาน

จะยังไม่ถือว่าเป็น Final Requirement จนกว่าจะได้รับการยืนยันจาก Stakeholder

---

# 7. Follow-up Backlog

- [x] ตรวจสอบ Traceability ระหว่าง Evidence → Need → Requirement
- [x] ตรวจสอบ Requirement ID ไม่ให้ซ้ำกัน
- [x] เพิ่ม Requirement สำหรับการจัดการปัญหาที่แจ้งซ้ำ
- [x] แยก Open Question ออกจาก Final Requirement
- [x] ตรวจสอบ MoSCoW Priority ของ Requirement
- [ ] ยืนยันเกณฑ์การกำหนดงาน Urgent
- [ ] ยืนยันผู้รับผิดชอบและผู้ยืนยันการปิดงาน
- [ ] ยืนยันวิธีจัดการรายการแจ้งปัญหาซ้ำ
- [ ] ยืนยันช่องทางการแจ้งเตือน
- [ ] ยืนยันรายงาน/สถิติที่ผู้บริหารต้องการ
- [ ] ยืนยัน Workflow การส่งต่องานระหว่างหน่วยงาน
- [ ] ตรวจสอบ SRS v1 หลังจาก Open Questions ได้รับคำตอบ

---

# 8. Validation Summary

จากการตรวจสอบ Requirements ใน Week 08 พบว่า Requirement หลักของระบบมีความสอดคล้องกับ Evidence และ Stakeholder Needs ในระดับที่สามารถนำไปพัฒนาต่อได้

อย่างไรก็ตาม Requirement บางรายการยังมีข้อมูลที่ต้องยืนยันเพิ่มเติม จึงถูกกำหนดสถานะเป็น `Needs Follow-up` แทนการกำหนดเป็น Final Requirement

โดยเฉพาะเรื่อง **การแจ้งปัญหาซ้ำ (Duplicate Maintenance Report)** ซึ่งต้องยืนยันก่อนว่าระบบควร:

1. รวมรายการแจ้งซ้ำเข้ากับรายการเดิม
2. เชื่อมรายการใหม่กับรายการเดิม
3. ปิดรายการใหม่ว่าเป็นรายการซ้ำ
4. หรือให้เจ้าหน้าที่เป็นผู้ตัดสินใจ

ดังนั้นทีมจะนำประเด็นดังกล่าวไปตรวจสอบกับ Stakeholder ก่อนนำไปกำหนดเป็น Workflow และ Acceptance Criteria ในขั้นตอนถัดไป
