# 07 — Software Requirements Specification (SRS) v2.1

> **Week 7 Deliverable (Complete Baseline Candidate)**  
> **Case:** ระบบแจ้งซ่อมอุปกรณ์ในห้องเรียนและห้องปฏิบัติการ (Classroom & Laboratory Maintenance Reporting System — CLMRS)  
> เวอร์ชัน: v2.1 | สถานะ: Baseline Candidate | วันที่: 22/09/2026

---

## 0. Document Control

| Version | Date | Author | Reviewer | Summary of Change |
|---|---|---|---|---|
| 0.1 | 21/09/2026 | Group 02 | [ระบุชื่อผู้ตรวจ] | Initial draft — สรุปจาก Requirement Backlog v0.2 และ Requirement Models (Week 06) |
| 1.0 | 21/09/2026 | Group 02 | [ระบุชื่อผู้ตรวจ] | Baseline candidate — เติมครบทุกหัวข้อ, ผูก Trace ไปยัง US / UC / AC |
| **2.1** | **22/09/2026** | **Group 02** | **[ระบุชื่อผู้ตรวจ]** | **Completed SRS — เพิ่ม CAP Mapping, State Matrix, Verification Plan, Review Gate, Disposition Table & AI Disclosure ตาม W07 Spec Example** |

| Field | Value |
|---|---|
| Course / Week | ENGSE206 / Week 07 |
| Team / Case No. | Group 02 / No.02 |
| W05 Source | Requirement Backlog v0.2: 9 FR / 1 NFR (Must 5, Should 4, Could 1, Won't yet 0) |
| W06 Source | Requirement Models: 15 US / 12 AC / 9 UC / 8 DR |

---

## 1. Introduction

### 1.1 Purpose
เอกสารนี้ระบุข้อกำหนดความต้องการของระบบ CLMRS ในรูปแบบที่ตรวจสอบย้อนกลับได้ (Traceable) จาก Evidence → Need → Requirement → User Story / Use Case / Acceptance Criteria เพื่อใช้เป็น input ของงานออกแบบสถาปัตยกรรม ฐานข้อมูล UX/UI และการทดสอบในขั้นถัดไป

SRS ฉบับนี้มีสถานะ **Baseline Candidate** ยังไม่ใช่ Approved Baseline เนื่องจากยังมี Open Issues ที่ต้องยืนยันกับ Stakeholder (ดูหัวข้อ 10)

### 1.2 Goals

| Goal | Outcome | Source | Status |
|---|---|---|---|
| G-01 | ผู้แจ้งซ่อมสามารถแจ้งปัญหาอุปกรณ์/ห้องเรียนผ่านช่องทางมาตรฐานและได้ Ticket ID ทันที | E-01, E-02 → N-01 | Accepted |
| G-02 | ข้อมูลการแจ้งซ่อมมีความครบถ้วน (อาคาร, ห้อง, หมวดหมู่, รายละเอียด) ก่อนส่งเข้าคิวงาน | E-03 → N-03 | Accepted |
| G-03 | งานที่มีความเร่งด่วน (Urgent) ได้รับการจัดลำดับให้ดำเนินการก่อน | E-04 → N-02 | Accepted |
| G-04 | ผู้แจ้งติดตามสถานะงานซ่อมของตนเองผ่าน Dashboard ได้ตลอดเวลา | E-05 → N-05 | Accepted |
| G-05 | กระบวนการซ่อมแซมและการปิดงานตรวจสอบย้อนหลังได้พร้อมผู้รับผิดชอบและผู้ยืนยัน | OQ-02 → N-02 | Accepted |
| G-06 | ป้องกันการเข้าถึงข้อมูลและฟังก์ชันข้ามสิทธิ์ของแต่ละบทบาท (Role-based Access) | E-NFR-01 → N-NFR-01 | Accepted |

### 1.3 Scope

**Core/Supporting Scope:**
- การกรอกและส่งฟอร์มแจ้งซ่อมมาตรฐานพร้อมไฟล์แนบ (FR-01, FR-02)
- การจัดลำดับคิวงานตามความเร่งด่วน (FR-03)
- การติดตามสถานะบน Dashboard (FR-04)
- การจัดการรายการแจ้งซ้ำ (FR-05)
- การบันทึกผลการซ่อมแซมและการปิดงานตาม Workflow (FR-06)
- การติดตามการส่งต่องานระหว่างหน่วยงาน (FR-07)
- การส่ง Notification แจ้งเตือน และรายงานสรุปสำหรับผู้บริหาร/ผู้ดูแลอาคาร (FR-08, FR-09)
- การควบคุมสิทธิ์การเข้าถึงแบบ Role-Based (NFR-01)

**Out of Scope:** ระบบจัดซื้ออะไหล่ / ระบบบริหารงบประมาณ / ระบบคลังวัสดุ / ระบบซ่อมอัตโนมัติ / การเชื่อมต่อระบบภายนอกมหาวิทยาลัย  
**Won't yet:** ไม่มี Requirement ที่ถูกตัดออกจากรอบนี้ | **Hold:** ไม่มี[cite: 3, 4, 5]

### 1.4 Capabilities Summary (CAP)

| CAP | Capability | Anchors / Requirements | W06 Models | Coverage Status |
|---|---|---|---|---|
| **CAP-01** | **Issue Reporting & Form Validation** | FR-CLMRS-01, FR-CLMRS-02; DR-01, DR-02 | US-01a, US-01b, US-02; UC-01; AC-01–04 | Detailed; Ready |
| **CAP-02** | **Work Queue & Priority Management** | FR-CLMRS-03, FR-CLMRS-05; DR-01, DR-03 | US-03, US-05; UC-03, UC-04; AC-05, AC-07 | Detailed with TBD (OQ-01, 03) |
| **CAP-03** | **Status Tracking & Dashboard** | FR-CLMRS-04; DR-01, DR-03 | US-04a, US-04b; UC-02; AC-06 | Detailed; Ready |
| **CAP-04** | **Execution, Transfer & Work Closure** | FR-CLMRS-06, FR-CLMRS-07; DR-04, DR-05 | US-06a, US-06b, US-07a, US-07b; UC-05, UC-06; AC-08, AC-09 | Detailed with TBD (OQ-02, 06) |
| **CAP-05** | **Notification & Reporting** | FR-CLMRS-08, FR-CLMRS-09; DR-06, DR-08 | US-08, US-09a, US-09b; UC-07, UC-08; AC-10, AC-11 | Partial / Extension |
| **CAP-06** | **Security & Access Control** | NFR-CLMRS-01; DR-07 | US-10; UC-09; AC-12 | Detailed; Cross-cutting |

---

## 2. Overall Description

### 2.1 Product Perspective
CLMRS เป็นระบบเว็บแอปพลิเคชันที่ผู้ใช้เข้าถึงได้ทั้งจากมือถือและคอมพิวเตอร์ (Responsive Design — AC-02) ทำหน้าที่เป็นช่องทางมาตรฐานช่องทางเดียวสำหรับการแจ้งซ่อม เพื่อลดปัญหาการแจ้งผ่านหลายช่องทาง (FR-CLMRS-01) โดยเก็บคำขอ สถานะ และประวัติการดำเนินงานไว้ในฐานข้อมูลกลาง

### 2.2 User Classes and Characteristics

| Actor | Role | Authorized Actions | Restrictions |
|---|---|---|---|
| **ACT-01** | **Student / Teacher (ผู้แจ้งซ่อม)** | กรอกฟอร์มแจ้งซ่อม, แนบรูปภาพ, ติดตามสถานะบน Dashboard, รับแจ้งเตือน | ไม่สามารถจัดการคิวงาน, ไม่เห็นคำขอของผู้อื่น, ไม่สามารถปิดงานซ่อม |
| **ACT-02** | **Technician (เจ้าหน้าที่เทคนิค)** | ดูคิวงาน, รับงาน, บันทึกการตรวจสอบ/รวมงานซ้ำ, ส่งต่องาน, บันทึกผลซ่อม และขอปิดงาน | ไม่สามารถอนุมัติปิดงานเองได้ (หากกติกากำหนดให้มีผู้ยืนยัน), ไม่เห็นรายงานผู้บริหาร |
| **ACT-03** | **Work Verifier (ผู้ยืนยันการปิดงาน)** | ตรวจสอบผลการดำเนินงานซ่อม, อนุมัติปิดงาน (Closed), ส่งกลับกรณีต้องแก้ไข | ไม่สามารถแก้ไขฟอร์มแจ้งซ่อมต้นทางได้ |
| **ACT-04** | **Building Manager / Admin** | ดูรายงานสรุปสถิติ, บริหารจัดการสิทธิ์และ Role Matrix | ไม่รับซ่อมงานโดยตรง |

### 2.3 Operating Environment
- ใช้งานผ่านเว็บเบราว์เซอร์บนอุปกรณ์มือถือและคอมพิวเตอร์ (Responsive Design — AC-02)
- เปิดใช้งานได้ตลอด 24 ชั่วโมงเมื่อเครือข่ายปกติ (AC-02)
- ข้อมูลทั้งหมดบันทึกลงฐานข้อมูลกลางของระบบ (AC-01)

### 2.4 Constraints
- **CON-01:** ควบคุมการเข้าถึงตาม Role (RBAC) หากพยายามข้ามสิทธิ์จะถูก Redirect ไป 403 Forbidden ภายใน 1 วินาที (NFR-01)
- **CON-02:** ไม่รวมระบบจัดซื้อ อะไหล่ งบประมาณ คลังวัสดุ และระบบภายนอกมหาวิทยาลัย
- **CON-03:** ไฟล์แนบรับเฉพาะ JPEG/PNG ขนาดไม่เกิน 5 MB (AC-04)
- **CON-04:** ห้ามผูกขาดช่องทางแจ้งเตือนเป็น LINE จนกว่าจะมี Evidence ยืนยัน (OQ-04)

---

## 3. Functional Requirements

| ID | Requirement | Priority | CAP | Acceptance / Verification | Traceability | Status |
|---|---|---|---|---|---|---|
| **FR-CLMRS-01** | ระบบต้องให้ผู้ใช้งานสามารถแจ้งปัญหาอุปกรณ์หรือห้องเรียน/ห้องปฏิบัติการที่ชำรุดผ่านช่องทางมาตรฐานของระบบได้ | **Must** | CAP-01 | บันทึกคำขอลงฐานข้อมูลและแสดง Ticket ID บนหน้าจอภายใน **3 วินาที** (AC-01); ฟอร์มเปิดใช้ได้ 24 ชม. และรองรับ Mobile/Desktop (AC-02) — **Test / Demo** | RC-F-01 → E-01, N-01 → US-01a, US-01b / UC-01 / AC-01, AC-02 | Ready for Week06 |
| **FR-CLMRS-02** | ระบบต้องให้ผู้แจ้งบันทึกข้อมูลที่จำเป็น เช่น อาคาร ห้อง รายละเอียดปัญหา และข้อมูลประกอบก่อนส่งคำขอ | **Must** | CAP-01 | แสดงสัญลักษณ์ (*) สีแดงกำกับ 4 ฟิลด์บังคับ; หากไม่ครบไม่อนุญาตให้ส่งและแจ้ง Pop-up ภายใน **1 วินาที** (AC-03); แนบไฟล์ JPEG/PNG ≤ 5 MB ได้พร้อม Preview (AC-04) — **Test** | RC-F-02 → E-02, E-03, N-03 → US-02 / UC-01 / AC-03, AC-04 | Needs Follow-up (OQ-07) |
| **FR-CLMRS-03** | ระบบต้องสนับสนุนการจัดลำดับความสำคัญของงานซ่อมตามระดับความเร่งด่วนที่กำหนด | **Must** | CAP-02 | จัดลำดับงานตามระดับความเร่งด่วนในคิวงาน โดยงาน Urgent จะถูกจัดขึ้นอันดับแรกอัตโนมัติ/โดยประเมิน (AC-05) — **Test** | RC-F-03 → E-04, N-02 → US-03 / UC-03 / AC-05 | Needs Follow-up (OQ-01) |
| **FR-CLMRS-04** | ระบบต้องให้ผู้ใช้งานสามารถตรวจสอบสถานะของรายการแจ้งซ่อมของตนเองได้ | **Must** | CAP-03 | Dashboard แสดงประวัติและสถานะปัจจุบัน (รับเรื่องแล้ว/กำลังดำเนินการ/ปิดงาน) ดึงข้อมูลเสร็จสิ้นภายใน **2 วินาที** (AC-06) — **Test / Demo** | RC-F-04 → E-05, N-05 → US-04a, US-04b / UC-02 / AC-06 | Ready for Week06 |
| **FR-CLMRS-05** | ระบบควรช่วยให้เจ้าหน้าที่สามารถตรวจสอบและจัดการรายการแจ้งปัญหาที่ซ้ำกันได้ | **Should** | CAP-02 | เจ้าหน้าที่ระบุ/รวมรายการที่ตรงกัน (อาคาร+ห้อง+ประเภทปัญหา) ภายใน Time Window ที่กำหนดเป็นรายการเดียวได้ (AC-07) — **Demo** | RC-F-06 → E-04, N-04 → US-05 / UC-04 / AC-07 | Needs Follow-up (OQ-03) |
| **FR-CLMRS-06** | ระบบควรให้เจ้าหน้าที่บันทึกผลการดำเนินงานและปิดงานซ่อม โดยมีผู้รับผิดชอบหรือผู้ยืนยันตาม Workflow | **Should** | CAP-04 | บันทึกผลซ่อม และมีชื่อผู้ดำเนินการ+ผู้ยืนยันตาม Workflow ก่อนเปลี่ยนสถานะเป็น "ปิดงาน" (AC-08) — **Test** | RC-F-05 → OQ-02, N-02 → US-06a, US-06b / UC-05 / AC-08 | Needs Follow-up (OQ-02) |
| **FR-CLMRS-07** | ระบบควรให้เจ้าหน้าที่สามารถติดตามสถานะของงานที่ถูกส่งต่อระหว่างหน่วยงานได้ | **Should** | CAP-04 | หน้าจอแสดงหน่วยงานที่รับผิดชอบปัจจุบันและประวัติการส่งต่อทั้งหมดใน Timeline เดียวกัน (AC-09) — **Demo** | RC-F-07 → OQ-06, N-07 → US-07a, US-07b / UC-06 / AC-09 | Needs Follow-up (OQ-06) |
| **FR-CLMRS-08** | ระบบควรแจ้งให้ผู้ใช้งานทราบเมื่อสถานะของงานซ่อมมีการเปลี่ยนแปลงตามช่องทางและเงื่อนไขที่ยืนยัน | **Could** | CAP-05 | ผู้ใช้ได้รับการแจ้งเตือนผ่านช่องทางที่ยืนยันเมื่อสถานะงานเปลี่ยนตามเงื่อนไข (AC-10) — **Test** | OQ-04 → OQ-04, N-05 → US-08 / UC-07 / AC-10 | Needs Follow-up (OQ-04) |
| **FR-CLMRS-09** | ระบบควรสนับสนุนรายงานและสถิติพื้นฐานของงานซ่อมสำหรับผู้ดูแลอาคารหรือผู้บริหาร | **Should** | CAP-05 | ดึงรายงานสรุปจำนวนงาน / สถานะ / ประเภทปัญหาย้อนหลังตามช่วงเวลาที่เลือกได้ (AC-11) — **Demo** | OQ-05 → OQ-05, N-06 → US-09a, US-09b / UC-08 / AC-11 | Needs Follow-up (OQ-05) |

---

## 4. Non-functional Requirements

| ID | Attribute | Requirement | Measure | Priority / Status |
|---|---|---|---|---|
| **NFR-CLMRS-01** | Security / Access | ควบคุมสิทธิ์การเข้าถึงข้อมูลตามบทบาทของผู้ใช้งาน (Student, Teacher, Tech, Verifier, Admin) | ปฏิเสธและ Redirect ไป **403 Forbidden ภายใน 1 วินาที** เมื่อเข้าถึง URL นอกสิทธิ์ (AC-12) | **Must** — Ready; Matrix detail in OQ-08 |
| **NFR-CLMRS-02** | Performance | ตอบสนองรวดเร็วในการทำงานหลัก | สร้าง Ticket ID ≤ 3s; เช็กฟิลด์ขาด ≤ 1s; โหลด Dashboard ≤ 2s | Proposed (Derived from AC-01/03/06) |
| **NFR-CLMRS-03** | Availability | ความพร้อมใช้งานของฟอร์มแจ้งซ่อม | เปิดใช้งานได้ 24 ชั่วโมงเมื่อเครือข่ายปกติ (AC-02) | Proposed (Derived from AC-02) |
| **NFR-CLMRS-04** | Usability | รองรับอุปกรณ์หลากหลาย | แสดงผลแบบ Responsive ทั้งมือถือและคอมพิวเตอร์ (AC-02) | Proposed (Derived from AC-02) |

---

## 5. Business Rules

| ID | Rule Statement | Authority | Priority | Status |
|---|---|---|---|---|
| **BR-01** | ฟิลด์ อาคาร, ห้อง, หมวดหมู่ปัญหา และรายละเอียดปัญหา ต้องมีค่าก่อนระบบยอมบันทึกคำขอ | Teaching Rule / FR-02 | Must | Provisional — OQ-07 |
| **BR-02** | ทุกคำขอที่บันทึกสำเร็จต้องได้ Ticket ID สำหรับอ้างอิงติดตามงาน | System Core / FR-01 | Must | Authorized |
| **BR-03** | ไฟล์แนบต้องเป็น JPEG/PNG ขนาดไม่เกิน 5 MB และไม่ถือเป็นฟิลด์บังคับ | System Constraint / AC-04 | Must | Authorized |
| **BR-04** | งานที่เข้าเกณฑ์ Urgent ต้องถูกจัดไว้อันดับแรกในคิวงานของเจ้าหน้าที่ | Workflow Rule / FR-03 | Must | Pending — OQ-01 |
| **BR-05** | ผู้แจ้งซ่อม (Student/Teacher) มีสิทธิ์เห็นเฉพาะรายการแจ้งซ่อมของตนเองบน Dashboard | Privacy Rule / UC-02 | Must | Authorized |
| **BR-06** | คำขอที่มีอาคาร+ห้อง+ประเภทปัญหาเดียวกันใน Time Window เดียวกัน ให้แสดงตัวเตือนรายการซ้ำ | Tech Rule / FR-05 | Should | Candidate — OQ-03 |
| **BR-07** | งานจะเปลี่ยนเป็น "ปิดงาน" (Closed) ได้ก็ต่อเมื่อมีบันทึกผลการซ่อมและผ่านการอนุมัติโดยผู้ยืนยัน | Quality Guard / FR-06 | Should | Pending — OQ-02 |
| **BR-08** | งานที่ถูกส่งต่อไปหน่วยงานอื่น ต้องแสดงหน่วยงานรับผิดชอบปัจจุบันและคงประวัติเดิมใน Timeline | Tracking Rule / FR-07 | Should | Pending — OQ-06 |

---

## 6. Data Requirements

รายการนี้เป็น **Conceptual Data Requirement** (อ้างอิง Domain Model)

| DR | Concept | Requirement Description | Classification | Traceability | W06 Use |
|---|---|---|---|---|---|
| **DR-01** | MaintenanceTicket | ระบบต้องเก็บ Ticket ID, ผู้แจ้ง, อาคาร, ห้อง, หมวดหมู่, รายละเอียด, ความเร่งด่วน, สถานะปัจจุบัน | Sensitive / Operations | FR-01, FR-02, FR-04 | UC-01, UC-02, UC-03 |
| **DR-02** | Attachment | ระบบต้องเก็บไฟล์ภาพแนบ (JPEG/PNG ≤ 5 MB) ผูกกับ MaintenanceTicket | Internal File | FR-02, AC-04 | UC-01; AC-04 |
| **DR-03** | TicketStatusLog | ระบบต้องเก็บประวัติการเปลี่ยนสถานะ เวลา และผู้เปลี่ยนสถานะ | Audit Log | FR-04, FR-06 | UC-02, UC-05 |
| **DR-04** | ExecutionRecord | ระบบต้องเก็บรายละเอียดการซ่อมแซม อะไหล่ที่ใช้ (ถ้ามี) และชื่อเจ้าหน้าที่เทคนิคผู้ซ่อม | Internal Operations | FR-06 | UC-05; AC-08 |
| **DR-05** | WorkVerification | ระบบต้องเก็บผลการตรวจงาน ชื่อผู้ยืนยันการปิดงาน และข้อติชม/เหตุผลการส่งกลับ | Quality Record | FR-06 | UC-05; AC-08 |
| **DR-06** | TransferHistory | ระบบต้องเก็บประวัติการส่งต่องาน หน่วยงานต้นทาง/ปลายทาง และเหตุผลการส่งต่อ | Operational Log | FR-07 | UC-06; AC-09 |
| **DR-07** | UserRoleAssignment | ระบบต้องเก็บ User Reference, Role, Permission Matrix และหน่วยงานที่สังกัด | Security Data | NFR-01 | UC-09; AC-12 |
| **DR-08** | SummaryReportData | ข้อมูลสรุปจำนวนงาน สัดส่วนสถานะ และประเภทปัญหาย้อนหลัง | Analytical Data | FR-09 | UC-08; AC-11 |

---

## 7. Behavioral Model References & State Transitions

### 7.1 บัญชีรับเข้า W06 (รหัสโมเดล)
- **User Stories (15 US):** US-01a, US-01b, US-02, US-03, US-04a, US-04b, US-05, US-06a, US-06b, US-07a, US-07b, US-08, US-09a, US-09b, US-10
- **Use Cases (9 UC):** UC-01, UC-02, UC-03, UC-04, UC-05, UC-06, UC-07, UC-08, UC-09
- **Acceptance Criteria (12 AC):** AC-01, AC-02, AC-03, AC-04, AC-05, AC-06, AC-07, AC-08, AC-09, AC-10, AC-11, AC-12

### 7.2 State Transition Matrix (การเปลี่ยนสถานะคำขอซ่อม)

| From State | Trigger Event | To State | Guard Condition / Action | Source |
|---|---|---|---|---|
| **[None]** | Press Submit Form | **Submitted** | Required 4 fields valid ➔ System generates Ticket ID[cite: 1, 4] | FR-01, BR-01, BR-02 |
| **Submitted** | Tech receives ticket | **In Progress** | Assigned to Technician queue (Urgent prioritized)[cite: 1, 4] | FR-03, BR-04 |
| **Submitted** | Duplicate found | **Merged / Closed** | Identified as duplicated ticket ➔ Linked to main ticket | FR-05, BR-06 |
| **In Progress** | Tech requests transfer | **Transferred** | Job requires other department ➔ Log transfer history | FR-07, BR-08 |
| **In Progress** | Tech submits fix | **Pending Verification** | Repair execution logged ➔ Sent to Work Verifier[cite: 1, 4] | FR-06, BR-07 |
| **Pending Verification**| Verifier approves | **Closed** | Work passes criteria ➔ Send Notification[cite: 1, 4] | FR-06, AC-08 |
| **Pending Verification**| Verifier rejects | **In Progress** | Work needs additional fix ➔ Send back to Tech[cite: 1, 4] | UC-05 Alt Flow |

---

## 8. External Interfaces

| ID | Interface Target | Direction | Purpose / Data Scope | TBD / Status |
|---|---|---|---|---|
| **EXT-01** | User Authentication Service | Inbound | ดึงข้อมูลผู้ใช้และ Role Claims เพื่อตรวจสอบสิทธิ์ | OAuth2/SSO Protocol = TBD (OQ-08) |
| **EXT-02** | Notification Gateway | Outbound | ส่งการแจ้งเตือนเมื่อสถานะเปลี่ยน (Email / App Notification) | Gateway Provider & Channel = TBD (OQ-04) |

---

## 9.Traceability and Coverage

| CAP ID | Capability Name | Requirements | W06 Use Cases | Coverage Status |
|---|---|---|---|---|
| **CAP-01** | Issue Reporting | FR-01, FR-02 | UC-01 | Detailed / Complete |
| **CAP-02** | Priority & Queue | FR-03, FR-05 | UC-03, UC-04 | Detailed with TBD |
| **CAP-03** | Status Tracking | FR-04 | UC-02 | Detailed / Complete |
| **CAP-04** | Execution & Closure | FR-06, FR-07 | UC-05, UC-06 | Detailed with TBD |
| **CAP-05** | Notification & Report | FR-08, FR-09 | UC-07, UC-08 | Partial / Extension |
| **CAP-06** | Access Control | NFR-01 | UC-09 | Detailed / Cross-cutting |

---

## 10. Open Issues (OQ Register)

| OI ID | Question / Open Issue | Impacted IDs | Owner | Next Action / Evidence Needed |
|---|---|---|---|---|
| **OQ-01** | เกณฑ์งาน Urgent คืออะไร และใครเป็นผู้กำหนด (ระบบหรือช่าง) | FR-03, UC-03, AC-05 | Tech Lead / Building Mgr | ยืนยัน Business Rule ของความเร่งด่วน |
| **OQ-02** | Role ผู้ยืนยันการปิดงานคือใคร (หัวหน้าช่าง/ผู้ดูแลอาคาร) | FR-06, UC-05, AC-08 | Building Mgr | ยืนยัน Approval Workflow |
| **OQ-03** | วิธีจัดการรายการแจ้งซ้ำและ Time Window ที่ใช้วัด | FR-05, UC-04, AC-07 | Tech Team | สรุป Logic การรวม/เชื่อมคำขอ |
| **OQ-04** | ช่องทาง และเงื่อนไขการส่ง Notification | FR-08, UC-07, AC-10 | System Analyst | เลือก Channel (Email/In-App) |
| **OQ-05** | ตัวชี้วัดรายงานและ KPI ที่ผู้บริหารต้องการ | FR-09, UC-08, AC-11 | Executive / Admin | กำหนด Layout และ Metric สรุป |
| **OQ-06** | Workflow การส่งต่องานระหว่างหน่วยงานและผู้รับผิดชอบหลัก | FR-07, UC-06, AC-09 | Tech Lead | ยืนยัน Cross-dept Policy |
| **OQ-07** | Required Fields ที่แท้จริงในการแจ้งซ่อม | FR-02, UC-01, AC-03 | Tech Team | ยืนยัน 4 ฟิลด์บังคับ |
| **OQ-08** | Permission Matrix และวิธี Auth SSO | NFR-01, UC-09, AC-12 | Security / IT | ออกแบบ Role-Permission Table |

---

## 11. Verification Plan

| VF ID | Method | Target | Procedure / Evidence | Owner |
|---|---|---|---|---|
| **VF-01** | **Review** | Traceability | ตรวจสอบความเชื่อมโยงผ่าน Trace Matrix (Evidence → Need → FR → UC → AC) | SA / Requirements Reviewer |
| **VF-02** | **Demonstration** | Core Workflows | สาธิตการเปิด Ticket (UC-01), ดู Dashboard (UC-02) และการซ่อมปิดงาน (UC-05) | Developer / Tester |
| **VF-03** | **Test** | Validation & Security | สั่ง Test Case บังคับกรอกข้อมูล (AC-03) และการบล็อกสิทธิ์ 403 Forbidden (AC-12) | QA Team |
| **VF-04** | **Inspection** | NFR & Data | ตรวจสอบโครงสร้าง Data Model (DR-01 ถึง DR-08) และการเก็บ log เปลี่ยนสถานะ | Database Admin / Security |

---

## 12. Review Gate

ผลการประเมินเอกสาร: **PASS — Baseline Candidate**
- **ข้อสรุป:** เอกสารประกอบด้วย 9 FR, 1 NFR หลัก (3 Proposed NFRs), 8 BR, 8 DR และเชื่อมโยงครบถ้วนกับ 15 US, 9 UC, 12 AC ใน Week 06
- **เงื่อนไข:** รายการ Open Issues (OQ-01 ถึง OQ-08) ต้องได้รับการยืนยันก่อนอนุมัติเป็น Approved Baseline สำหรับการเริ่มพัฒนาระบบจริง

---

## Appendix A — Requirement Disposition

| Requirement ID | Disposition | SRS Location | Reason / Status |
|---|---|---|---|
| **FR-CLMRS-01** | **Included** | หัวข้อ 3 | Core Scope (Must) — Ready for Baseline |
| **FR-CLMRS-02** | **Included** | หัวข้อ 3 | Core Scope (Must) — Pending OQ-07 |
| **FR-CLMRS-03** | **Included** | หัวข้อ 3 | Core Scope (Must) — Pending OQ-01 |
| **FR-CLMRS-04** | **Included** | หัวข้อ 3 | Core Scope (Must) — Ready for Baseline |
| **FR-CLMRS-05** | **Included** | หัวข้อ 3 | Supporting (Should) — Pending OQ-03 |
| **FR-CLMRS-06** | **Included** | หัวข้อ 3 | Supporting (Should) — Pending OQ-02 |
| **FR-CLMRS-07** | **Included** | หัวข้อ 3 | Supporting (Should) — Pending OQ-06 |
| **FR-CLMRS-08** | **Partial / Extension** | หัวข้อ 3 | Optional (Could) — Pending OQ-04 |
| **FR-CLMRS-09** | **Included** | หัวข้อ 3 | Supporting (Should) — Pending OQ-05 |
| **NFR-CLMRS-01** | **Included** | หัวข้อ 4 | Security Core (Must) — Pending OQ-08 |
| **NFR-CLMRS-02..04**| **Proposed** | หัวข้อ 4 | Derived from AC-01/02/03/06 |

---

## Appendix B — AI Use Disclosure

<<<<<<< HEAD
เอกสาร SRS v2.1 ฉบับนี้ได้รับการสนับสนุนการจัดทำโดย AI (Gemini) ในกระบวนการดังต่อไปนี้:[cite: 6]
1. ตรวจสอบความถูกต้องและสอดคล้องของการอ้างอิงย้อนกลับ (Traceability) ระหว่าง Requirement Backlog v0.2[cite: 3], Requirement Models Week 06[cite: 4] และโครงสร้าง SRS[cite: 5]
2. จัดเรียงตารางข้อมูล CAP Mapping[cite: 6], State Transition Matrix[cite: 6], Verification Plan[cite: 6] และ Requirement Disposition Table ให้ตรงตาม Teaching Template (ENGSE206 Week 07 Example)[cite: 6]
3. **การยืนยันข้อมูล:** เนื้อหา ตรรกะของระบบ ขอบเขตงาน และการตัดสินใจเกี่ยวกับระบบ CLMRS ทั้งหมดได้รับการตรวจสอบและอนุมัติโดยสมาชิกกลุ่ม Group 02 เรียบร้อยแล้ว[cite: 5, 6]
=======
เอกสาร SRS v2.1 ฉบับนี้ได้รับการสนับสนุนการจัดทำโดย AI (Gemini) ในกระบวนการดังต่อไปนี้:
1. ตรวจสอบความถูกต้องและสอดคล้องของการอ้างอิงย้อนกลับ (Traceability) ระหว่าง Requirement Backlog v0.2, Requirement Models Week 06 และโครงสร้าง SRS
2. จัดเรียงตารางข้อมูล CAP Mapping, State Transition Matrix, Verification Plan และ Requirement Disposition Table ให้ตรงตาม Teaching Template (ENGSE206 Week 07 Example)
3. **การยืนยันข้อมูล:** เนื้อหา ตรรกะของระบบ ขอบเขตงาน และการตัดสินใจเกี่ยวกับระบบ CLMRS ทั้งหมดได้รับการตรวจสอบและอนุมัติโดยสมาชิกกลุ่ม Group 02 เรียบร้อยแล้ว
>>>>>>> 8762929 (Implement feature X to enhance user experience and optimize performance)
