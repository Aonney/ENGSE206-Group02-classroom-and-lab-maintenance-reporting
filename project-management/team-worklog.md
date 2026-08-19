# Team Worklog

> **Team:** Group 02 — Classroom & Laboratory Maintenance Reporting System
> **Case:** No.02
> **Members:** นายสันติ ปัญญาหน้อย / นายธีรนัย ไชยกันทะ / นายบูรพา ประทีปรัตน์
>
> บันทึกการทำงานของสมาชิกในแต่ละสัปดาห์ โดยแต่ละรายการต้องเชื่อมโยงกับ Artefact หรือหลักฐานของงานที่ทำจริงใน Repository

---

## Week 01 — Problem Brief

**ช่วงงาน:** Week 01
**เป้าหมาย:** ทำความเข้าใจปัญหา วิเคราะห์ Facts, Pain Points, Stakeholders และกำหนด Scope เบื้องต้น

| Date       | Member               | Task / Contribution                                                | Artefact / File Changed         | Commit / Evidence Link | Time Spent | Status |
| ---------- | -------------------- | ------------------------------------------------------------------ | ------------------------------- | ---------------------- | ---------: | ------ |
| 06/07/2026 | นายสันติ ปัญญาหน้อย  | วิเคราะห์ Problem Statement, Facts และ Pain Points ของระบบแจ้งซ่อม | `docs/01-problem-brief-v0.1.md` | `[commit hash]`        |       2 hr | Done   |
| 06/07/2026 | นายธีรนัย ไชยกันทะ   | วิเคราะห์ Stakeholder และ User Needs เบื้องต้น                     | `docs/01-problem-brief-v0.1.md` | `[commit hash]`        |       2 hr | Done   |
| 06/07/2026 | นายบูรพา ประทีปรัตน์ | ทบทวน Scope, Goals, Assumptions และ Open Questions                 | `docs/01-problem-brief-v0.1.md` | `[commit hash]`        |       2 hr | Done   |

### Week 01 Outcome

ทีมได้ Problem Brief ที่ระบุปัญหาหลักของระบบ ได้แก่ การแจ้งปัญหาหลายช่องทาง ข้อมูลไม่ครบ การแจ้งซ้ำ การติดตามสถานะที่ทำได้ยาก และการส่งต่องานหลายหน่วยงาน

**ผลลัพธ์หลัก**

* Problem Statement
* Facts / Pain Points
* Initial Stakeholders
* Initial Goals
* Initial Scope
* Initial User Needs
* Assumptions และ Open Questions

---

# Week 02 — Stakeholder, Context and Scope

**วันที่หลัก:** 13/07/2026
**เป้าหมาย:** วิเคราะห์ Stakeholder ให้ละเอียด กำหนด System Context และปรับ Scope

| Date       | Member               | Task / Contribution                                                      | Artefact / File Changed                                     | Commit / Evidence Link | Time Spent | Status |
| ---------- | -------------------- | ------------------------------------------------------------------------ | ----------------------------------------------------------- | ---------------------- | ---------: | ------ |
| 13/07/2026 | นายสันติ ปัญญาหน้อย  | วิเคราะห์ Stakeholder Profiles และปรับ Problem Frame                     | `docs/02-stakeholder-context-scope.md`                      | `[commit hash]`        |       2 hr | Done   |
| 13/07/2026 | นายธีรนัย ไชยกันทะ   | ออกแบบ System Context Diagram และวิเคราะห์ Data Flow                     | `diagrams/context/w02-system-context.drawio` / `.png`       | `[commit hash]`        |     2.5 hr | Done   |
| 13/07/2026 | นายธีรนัย ไชยกันทะ   | ออกแบบ Stakeholder Map และจัดกลุ่มผู้มีส่วนได้ส่วนเสีย                   | `diagrams/stakeholders/w02-stakeholder-map.drawio` / `.png` | `[commit hash]`        |       2 hr | Done   |
| 13/07/2026 | นายบูรพา ประทีปรัตน์ | ตรวจสอบความถูกต้องของ Stakeholder, Scope และรับ Feedback จาก Peer Review | `feedback/week-02-peer-feedback.md`                         | `[commit hash]`        |       2 hr | Done   |

### Week 02 Outcome

ทีมปรับ Stakeholder Profiles ให้มี Goal, Pain Point, Concern, Influence และ Open Questions รวมถึงกำหนด System Boundary, In Scope, Out of Scope และ Constraints ให้ชัดเจนขึ้น

**สิ่งที่ยังต้องค้นหาใน Week ถัดไป**

* เกณฑ์การกำหนด Urgent
* ผู้มีอำนาจปิดงาน
* วิธีจัดการ Duplicate Report
* ช่องทาง Notification
* รูปแบบ Report / KPI

---

# Week 03 — Elicitation Planning

**วันที่หลัก:** 20/07/2026
**เป้าหมาย:** วางแผนการเก็บข้อมูลจาก Stakeholders เพื่อยืนยัน Open Questions และเตรียม Evidence สำหรับ Requirement

| Date       | Member               | Task / Contribution                                               | Artefact / File Changed       | Commit / Evidence Link | Time Spent | Status |
| ---------- | -------------------- | ----------------------------------------------------------------- | ----------------------------- | ---------------------- | ---------: | ------ |
| 20/07/2026 | นายสันติ ปัญญาหน้อย  | วิเคราะห์ Open Questions จาก Week 02 และจัดลำดับความสำคัญของคำถาม | `docs/03-elicitation-plan.md` | `[commit hash]`        |       2 hr | Done   |
| 20/07/2026 | นายธีรนัย ไชยกันทะ   | จัดทำ Interview Questions สำหรับ Student / Teacher / Technician   | `docs/03-interview-guide.md`  | `[commit hash]`        |     2.5 hr | Done   |
| 20/07/2026 | นายบูรพา ประทีปรัตน์ | กำหนด Evidence ที่ต้องการเก็บและผู้รับผิดชอบการเก็บข้อมูล         | `docs/03-elicitation-plan.md` | `[commit hash]`        |       2 hr | Done   |
| 20/07/2026 | นายบูรพา ประทีปรัตน์ | ตรวจสอบความครอบคลุมของคำถามกับ Stakeholder และ Open Questions     | `docs/03-interview-guide.md`  | `[commit hash]`        |     1.5 hr | Done   |

### Week 03 Outcome

ทีมกำหนดวิธีเก็บข้อมูล ผู้ให้ข้อมูล หลักฐานที่ต้องการ และผู้รับผิดชอบ เพื่อเตรียมยืนยัน Requirement ใน Week 04

**Artefacts หลัก**

* `docs/03-elicitation-plan.md`
* `docs/03-interview-guide.md`

---

# Week 04 — Evidence, Requirement Candidates and Negotiation

**เป้าหมาย:** เปลี่ยน Evidence ให้เป็น Requirement Candidates และบันทึกผลการเจรจา/Conflict ระหว่าง Stakeholders

| Date       | Member               | Task / Contribution                                                 | Artefact / File Changed                                         | Commit / Evidence Link | Time Spent | Status |
| ---------- | -------------------- | ------------------------------------------------------------------- | --------------------------------------------------------------- | ---------------------- | ---------: | ------ |
| 27/07/2026 | นายสันติ ปัญญาหน้อย  | รวบรวมและจัดหมวดหมู่ Evidence จากการ Elicitation                    | `docs/04-evidence-log.md`                                       | `[commit hash]`        |       2 hr | Done   |
| 27/07/2026 | นายธีรนัย ไชยกันทะ   | วิเคราะห์ Evidence → Need → Requirement Candidate                   | `docs/04-requirement-candidates.md`                             | `[commit hash]`        |     2.5 hr | Done   |
| 27/07/2026 | นายบูรพา ประทีปรัตน์ | วิเคราะห์ Conflict ระหว่าง Stakeholders และจัดทำ Negotiation Record | `docs/04-negotiation-record.md`                                 | `[commit hash]`        |       2 hr | Done   |
| 27/07/2026 | นายสันติ ปัญญาหน้อย  | ตรวจสอบ Traceability ของ E-ID, Need และ RC-ID                       | `docs/04-evidence-log.md` / `docs/04-requirement-candidates.md` | `[commit hash]`        |       2 hr | Done   |
| 27/07/2026 | นายธีรนัย ไชยกันทะ   | ทบทวน Requirement Candidates และระบุรายการที่ต้อง Needs Validation  | `docs/04-requirement-candidates.md`                             | `[commit hash]`        |     1.5 hr | Done   |

### Week 04 Outcome

ทีมแปลง Evidence เป็น Requirement Candidates โดยยึดหลัก **Evidence → Need → Requirement Candidate** และไม่สร้าง Evidence ที่ไม่มีหลักฐานรองรับ

Requirement Candidates หลักที่ได้ ได้แก่:

* `RC-F-01` — แจ้งปัญหา
* `RC-F-02` — บันทึกข้อมูลที่จำเป็น
* `RC-F-03` — จัดลำดับความเร่งด่วน
* `RC-F-04` — ติดตามสถานะ
* `RC-F-05` — บันทึกผลและปิดงาน
* `RC-F-06` — จัดการรายการแจ้งซ้ำ
* `RC-F-07` — ติดตามงานส่งต่อ
* `RC-F-08` — รายงานและสถิติ

ในส่วน Negotiation ทีมบันทึก 3 ประเด็นหลัก ได้แก่ Complete Information, Duplicate Report และ Work Assignment / Final Close โดยประเด็นการปิดงานยังเป็น **Unresolved** และต้องมีการตรวจสอบเพิ่มเติม

---

# Week 05 — Prioritization and Requirement Backlog

**เป้าหมาย:** จัดลำดับ Requirement, ตรวจสอบ Traceability, บันทึก Open Questions และจัดทำ Requirement Backlog

| Date       | Member               | Task / Contribution                                                 | Artefact / File Changed                                                                            | Commit / Evidence Link | Time Spent | Status |
| ---------- | -------------------- | ------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | ---------------------- | ---------: | ------ |
| 03/08/2026 | นายสันติ ปัญญาหน้อย  | จัดทำ Open Questions และ Issues จาก Requirement ที่ยังไม่ยืนยัน     | `docs/05-open-questions-and-issues.md`                                                             | `[commit hash]`        |       2 hr | Done   |
| 03/08/2026 | นายธีรนัย ไชยกันทะ   | จัดทำ Prioritization โดยพิจารณา Value, Risk, Urgency และ Dependency | `docs/05-prioritization-rationale.md`                                                              | `[commit hash]`        |     2.5 hr | Done   |
| 03/08/2026 | นายบูรพา ประทีปรัตน์ | จัดทำและตรวจสอบ Requirement Backlog                                 | `docs/05-requirement-backlog.md`                                                                   | `[commit hash]`        |     2.5 hr | Done   |
| 04/08/2026 | นายสันติ ปัญญาหน้อย  | ตรวจสอบ Req ID และ Priority ให้ตรงกันระหว่าง Backlog และ Rationale  | `docs/05-requirement-backlog.md` / `docs/05-prioritization-rationale.md`                           | `[commit hash]`        |       2 hr | Done   |
| 04/08/2026 | นายธีรนัย ไชยกันทะ   | ตรวจสอบ Evidence → Need → RC → Requirement Traceability             | `docs/04-evidence-log.md` / `docs/04-requirement-candidates.md` / `docs/05-requirement-backlog.md` | `[commit hash]`        |       2 hr | Done   |
| 04/08/2026 | นายบูรพา ประทีปรัตน์ | ตรวจสอบ Acceptance Measure และสถานะ Ready / Needs Follow-up / Hold  | `docs/05-requirement-backlog.md`                                                                   | `[commit hash]`        |       2 hr | Done   |

### Week 05 Outcome

ทีมจัดลำดับ Requirement โดยใช้ Value, Risk, Urgency และ Dependency และตรวจสอบให้ Req ID / Priority สอดคล้องกันระหว่างเอกสาร

### Requirement Priority

**Must**

* `FR-CLMRS-01` — แจ้งปัญหา
* `FR-CLMRS-02` — บันทึกข้อมูลที่จำเป็น
* `FR-CLMRS-03` — จัดลำดับความเร่งด่วน
* `FR-CLMRS-04` — ติดตามสถานะ
* `NFR-CLMRS-01` — ควบคุมสิทธิ์ตามบทบาท

**Should**

* `FR-CLMRS-05` — จัดการรายการแจ้งซ้ำ
* `FR-CLMRS-06` — บันทึกผลและปิดงาน
* `FR-CLMRS-07` — ติดตามงานส่งต่อ
* `FR-CLMRS-09` — รายงานและสถิติ

**Could**

* `FR-CLMRS-08` — การแจ้งเตือน

การจัด Priority ดังกล่าวตรงกับ `docs/05-prioritization-rationale.md` ซึ่งระบุ Must 5 รายการ, Should 4 รายการ และ Could 1 รายการ

---

# Weekly Summary

| Week    | Topic                         | Main Deliverable                                                                 | Main Result                                                     |
| ------- | ----------------------------- | -------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| Week 01 | Problem Understanding         | `01-problem-brief-v0.1.md`                                                       | วิเคราะห์ปัญหา Stakeholder, Goals และ Scope                     |
| Week 02 | Stakeholder / Context / Scope | `02-stakeholder-context-scope.md`                                                | กำหนด Stakeholder, System Boundary และ Scope                    |
| Week 03 | Elicitation                   | `03-elicitation-plan.md`, `03-interview-guide.md`                                | วางแผนเก็บ Evidence และคำถามสัมภาษณ์                            |
| Week 04 | Evidence / Requirements       | `04-evidence-log.md`, `04-requirement-candidates.md`, `04-negotiation-record.md` | แปลง Evidence เป็น Requirement Candidates และบันทึก Negotiation |
| Week 05 | Prioritization / Backlog      | `05-prioritization-rationale.md`, `05-requirement-backlog.md`                    | จัด Priority และสร้าง Requirement Backlog                       |
| Week 06 | Requirement Models            | `06-requirement-models.md`                                                       | User Stories, Use Cases และ Acceptance Criteria                 |
| Week 07 | SRS                           | `07-srs-v1.md`                                                                   | รวม Requirement เป็น SRS                                        |
| Week 08 | Validation / Traceability     | `08-validation-traceability.md`                                                  | ตรวจสอบ Requirement และ Traceability                            |

> **หมายเหตุ:** Week 06–08 ถูกใส่ไว้เป็น Project Roadmap เท่านั้น เพราะจากเอกสารที่ตรวจพบ `06-requirement-models.md` ยังเป็น Template และระบุว่าเป็น Week 6 deliverable จึงไม่ควรสร้าง Worklog ว่าทำเสร็จแล้วโดยไม่มีหลักฐานจริง

---

# Worklog Rules

1. ทุกคนควรมีงานอย่างน้อย 1 รายการต่อสัปดาห์เมื่อมีงานของรายวิชา
2. งานทุกชิ้นควรอ้างอิง Artefact ที่ตรวจสอบได้
3. ห้ามสร้าง Commit Hash หรือ Evidence Link ขึ้นมาเอง
4. หากยังไม่มี Commit ให้ใช้ `[commit hash]` จนกว่าจะนำ Hash จริงมาใส่
5. หาก Requirement ยังไม่มี Evidence เพียงพอ ให้ระบุเป็น `Needs Validation` หรือ `Open Question`
6. Worklog ต้องสอดคล้องกับเอกสาร Requirements และ SRS ใน Repository

---

# Current Status

**Week 01–05:** Completed / Documented

**Week 06:** Requirement Modeling — เตรียมดำเนินการ

**Week 07:** SRS — เตรียมดำเนินการ

**Week 08:** Validation & Traceability — เตรียมดำเนินการ

Last updated: `19/08/2026`
