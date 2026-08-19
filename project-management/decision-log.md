# Decision Log

> ใช้สำหรับบันทึกการตัดสินใจของทีมที่มีผลต่อ Problem Scope, Stakeholder, Requirement, Prioritization และการจัดทำเอกสารของโครงงาน
>
> **Project:** Classroom & Laboratory Maintenance Reporting System
> **Case:** No.02
> **Team:** Group 02
> **Members:** นายสันติ ปัญญาหน้อย / นายธีรนัย ไชยกันทะ / นายบูรพา ประทีปรัตน์

---

## Decision Records

| ID     | Week    | Date       | Decision                                                                                                         | Options Considered                                                       | Rationale                                                                                             | Impacted Artefacts                                                                                                                      | Owner                | Status   |
| ------ | ------- | ---------- | ---------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | -------------------- | -------- |
| `D-01` | Week 01 | 04/08/2026 | กำหนดปัญหาหลักของโครงงานเป็นการแจ้งซ่อมที่กระจัดกระจาย ข้อมูลไม่ครบ และติดตามสถานะได้ยาก                         | A: ทำระบบแจ้งซ่อม / B: ทำระบบ Inventory / C: ทำระบบจัดซื้อ               | Problem Brief ระบุว่าปัญหาหลักอยู่ที่กระบวนการแจ้งและติดตามงานซ่อม จึงเลือกเน้น Maintenance Reporting | `docs/01-problem-brief-v0.1.md`                                                                                                         | นายสันติ ปัญญาหน้อย  | Accepted |
| `D-02` | Week 01 | 04/08/2026 | กำหนด Stakeholders หลักเป็น นักศึกษา/ผู้ใช้งานห้อง, อาจารย์, เจ้าหน้าที่เทคนิค และผู้ดูแลอาคาร/ผู้บริหาร         | A: จำกัดเฉพาะนักศึกษา / B: รวมผู้เกี่ยวข้องทุกฝ่าย / C: เฉพาะเจ้าหน้าที่ | แต่ละกลุ่มมีเป้าหมายและ Pain Point แตกต่างกัน และมีผลต่อกระบวนการแจ้งซ่อม                             | `docs/01-problem-brief-v0.1.md`                                                                                                         | นายธีรนัย ไชยกันทะ   | Accepted |
| `D-03` | Week 01 | 04/08/2026 | กำหนด In Scope ให้ครอบคลุมการแจ้งปัญหา บันทึกข้อมูล มอบหมาย/ติดตามงาน จัดลำดับความเร่งด่วน ปิดงาน และรายงานสถิติ | A: เฉพาะแจ้งซ่อม / B: ครบกระบวนการ Maintenance / C: รวมจัดซื้อและคลัง    | ต้องครอบคลุม Workflow หลัก แต่ไม่ขยายไปยังระบบจัดซื้อ งบประมาณ และคลังวัสดุ                           | `docs/01-problem-brief-v0.1.md`                                                                                                         | นายบูรพา ประทีปรัตน์ | Accepted |
| `D-04` | Week 02 | 13/07/2026 | แยกระบบ Maintenance Reporting ออกจากระบบจัดซื้อ งบประมาณ และคลังวัสดุ                                            | A: รวมทุกระบบ / B: Maintenance Reporting เท่านั้น                        | เพื่อควบคุมขอบเขตให้เหมาะกับโครงงานรายวิชาและลดความซับซ้อน                                            | `docs/02-stakeholder-context-scope.md`                                                                                                  | นายสันติ ปัญญาหน้อย  | Accepted |
| `D-05` | Week 02 | 13/07/2026 | กำหนดให้ระบบรองรับผู้ใช้งานหลายบทบาท                                                                             | A: ทุกคนใช้สิทธิ์เดียวกัน / B: แบ่งสิทธิ์ตามบทบาท                        | Problem Brief ระบุว่าผู้ใช้งานมีหลายบทบาทและต้องป้องกันการเข้าถึงข้อมูลตามสิทธิ์                      | `docs/02-stakeholder-context-scope.md`                                                                                                  | นายธีรนัย ไชยกันทะ   | Accepted |
| `D-06` | Week 03 | 20/07/2026 | ใช้การสัมภาษณ์/สอบถาม Stakeholders เป็นแนวทางหลักในการเก็บข้อมูล Requirement                                     | A: เดา Requirement จากระบบเดิม / B: Interview / C: สร้าง Prototype ก่อน  | Open Questions หลายข้อเกี่ยวข้องกับ Business Rules ที่ต้องยืนยันจากผู้เกี่ยวข้องก่อน                  | `docs/03-elicitation-plan.md`, `docs/03-interview-guide.md`                                                                             | นายธีรนัย ไชยกันทะ   | Accepted |
| `D-07` | Week 03 | 20/07/2026 | ให้ความสำคัญกับคำถามเรื่อง Urgent Criteria, Duplicate Report, การปิดงาน และการส่งต่องาน                          | A: ถามทุกประเด็นเท่ากัน / B: เน้น Open Questions ที่กระทบ Requirement    | ประเด็นเหล่านี้ส่งผลโดยตรงต่อ Workflow และ Acceptance Criteria                                        | `docs/03-elicitation-plan.md`, `docs/03-interview-guide.md`                                                                             | นายบูรพา ประทีปรัตน์ | Accepted |
| `D-08` | Week 04 | 27/07/2026 | ใช้ Traceability แบบ Evidence → Need → Requirement Candidate                                                     | A: สร้าง Requirement โดยตรง / B: Evidence → Need → RC                    | เพื่อป้องกัน Requirement ที่ไม่มีหลักฐานรองรับและสามารถตรวจสอบย้อนกลับได้                             | `docs/04-evidence-log.md`, `docs/04-requirement-candidates.md`                                                                          | นายธีรนัย ไชยกันทะ   | Accepted |
| `D-09` | Week 04 | 27/07/2026 | ไม่สรุป Business Rule ที่ยังไม่มี Evidence ให้เป็น Requirement แบบตายตัว                                         | A: ตัดสินใจทันที / B: เก็บเป็น Open Question / Needs Validation          | เกณฑ์ Urgent, Duplicate Handling และการปิดงานยังต้องมีข้อมูลยืนยันเพิ่มเติม                           | `docs/04-evidence-log.md`, `docs/04-negotiation-record.md`                                                                              | นายสันติ ปัญญาหน้อย  | Accepted |
| `D-10` | Week 04 | 27/07/2026 | บันทึกประเด็นที่ Stakeholders อาจมีความเห็นต่างไว้ใน Negotiation Record แทนการเลือกฝ่ายใดฝ่ายหนึ่งทันที          | A: เลือกตามความคิดเห็นส่วนใหญ่ / B: บันทึก Conflict และหา Evidence เพิ่ม | ทำให้การตัดสินใจสามารถตรวจสอบย้อนกลับได้และลดการเดา Requirement                                       | `docs/04-negotiation-record.md`                                                                                                         | นายบูรพา ประทีปรัตน์ | Accepted |
| `D-11` | Week 05 | 03/08/2026 | จัด Priority ของ Requirement โดยใช้ Must / Should / Could                                                        | A: ทุก Requirement เป็น Must / B: MoSCoW                                 | ช่วยแยก Requirement ที่จำเป็นต่อระบบออกจาก Requirement ที่สามารถทำภายหลังได้                          | `docs/05-prioritization-rationale.md`, `docs/05-requirement-backlog.md`                                                                 | นายธีรนัย ไชยกันทะ   | Accepted |
| `D-12` | Week 05 | 03/08/2026 | กำหนด Must Requirements จำนวน 5 รายการ ได้แก่ FR-CLMRS-01 ถึง FR-CLMRS-04 และ NFR-CLMRS-01                       | A: ให้ทุก Functional Requirement เป็น Must / B: คัดเฉพาะความต้องการหลัก  | เลือกจาก Value, Risk, Urgency และ Dependency ของระบบ                                                  | `docs/05-prioritization-rationale.md`, `docs/05-requirement-backlog.md`                                                                 | นายสันติ ปัญญาหน้อย  | Accepted |
| `D-13` | Week 05 | 04/08/2026 | Requirement ที่ยังมีข้อมูลไม่เพียงพอให้ระบุสถานะ Needs Follow-up หรือ Needs Validation แทนการยืนยันเป็น Ready    | A: Mark Ready ทั้งหมด / B: แยกสถานะตาม Evidence                          | ช่วยให้ Backlog สะท้อนระดับความมั่นใจของ Requirement และเห็นงานที่ต้องตรวจสอบต่อ                      | `docs/05-requirement-backlog.md`                                                                                                        | นายบูรพา ประทีปรัตน์ | Accepted |
| `D-14` | Week 05 | 04/08/2026 | ตรวจสอบ Req ID, Priority และ Traceability ให้ตรงกันระหว่าง Requirement Candidates, Prioritization และ Backlog    | A: แก้เฉพาะ Backlog / B: ตรวจสอบเอกสารที่เกี่ยวข้องทั้งหมด               | Requirement ID และ Evidence Mapping ต้องสอดคล้องกันทั้งชุดเอกสารก่อนทำ Baseline                       | `docs/04-requirement-candidates.md`, `docs/04-evidence-log.md`, `docs/05-prioritization-rationale.md`, `docs/05-requirement-backlog.md` | นายธีรนัย ไชยกันทะ   | Accepted |

---

# Decision Details

## D-01 — กำหนด Problem Frame

ทีมตัดสินใจให้โครงงานมุ่งแก้ปัญหา **กระบวนการแจ้งและติดตามงานซ่อมอุปกรณ์ในห้องเรียนและห้องปฏิบัติการ** เนื่องจาก Problem Brief พบปัญหาการแจ้งผ่านหลายช่องทาง ข้อมูลไม่ครบ การแจ้งซ้ำ และการติดตามสถานะทำได้ยาก

จึงไม่ขยายโครงงานไปเป็นระบบบริหารทรัพยากรหรือระบบจัดซื้อ

**ผลกระทบ:** เป็นพื้นฐานสำหรับ Scope และ Requirement ทั้งหมด

---

## D-02 — Stakeholder หลัก

ทีมกำหนด Stakeholder หลัก 4 กลุ่ม:

1. นักศึกษา / ผู้ใช้งานห้อง
2. อาจารย์ผู้สอน
3. เจ้าหน้าที่เทคนิค
4. ผู้ดูแลอาคาร / ผู้บริหาร

เหตุผลคือแต่ละกลุ่มได้รับผลกระทบจากปัญหาและมีเป้าหมายต่อระบบแตกต่างกัน โดย Problem Brief ระบุเป้าหมายและความกังวลของแต่ละกลุ่มไว้อย่างชัดเจน

---

## D-03 — Scope

ทีมกำหนดให้ระบบครอบคลุม:

* การแจ้งปัญหา
* การบันทึกข้อมูล
* การมอบหมายงาน
* การจัดลำดับความเร่งด่วน
* การติดตามสถานะ
* การบันทึกผลและปิดงาน
* รายงานสถิติ

และไม่นำระบบจัดซื้อ งบประมาณ คลังวัสดุ และระบบภายนอกของมหาวิทยาลัยเข้ามาอยู่ใน Scope

---

## D-04 — System Boundary

เพื่อควบคุมขอบเขตของโครงงาน ทีมแยก **Maintenance Reporting System** ออกจากระบบสนับสนุนอื่น ๆ เช่น Procurement และ Inventory

หากมีความต้องการเชื่อมต่อระบบภายนอก จะถือเป็น Out of Scope ในระยะนี้

---

## D-05 — Role-based Access

ทีมตัดสินใจว่าระบบควรรองรับการใช้งานหลายบทบาทและควบคุมสิทธิ์ตาม Role เนื่องจากนักศึกษา อาจารย์ เจ้าหน้าที่เทคนิค และผู้ดูแลอาคารมีหน้าที่และข้อมูลที่ต้องเข้าถึงแตกต่างกัน

---

## D-06 — Elicitation Method

ทีมเลือกใช้ Interview / Structured Questions เป็นวิธีหลักในการเก็บข้อมูลเพิ่มเติม เนื่องจากยังมี Open Questions ที่ไม่สามารถสรุปจาก Case Card ได้ เช่น:

* เกณฑ์ Urgent
* ผู้อนุมัติการปิดงาน
* การจัดการ Duplicate
* Notification
* Report / KPI
* งานที่ส่งต่อหลายหน่วยงาน

---

## D-07 — Evidence First

ทีมตกลงว่า Requirement ที่สำคัญต้องสามารถย้อนกลับไปหา Evidence และ Stakeholder Need ได้

รูปแบบ Traceability ที่ใช้คือ:

`Evidence → Need → Requirement Candidate → Requirement`

วิธีนี้ช่วยลดการสร้าง Requirement จากการคาดเดาของทีม

---

## D-08 — Unresolved Business Rules

ทีมจะไม่ตัดสินใจแทน Stakeholder ในเรื่องที่ยังไม่มี Evidence เพียงพอ

ตัวอย่างเช่น:

* ใครเป็นผู้ยืนยันการปิดงาน
* งานใดถือว่า Urgent
* Duplicate Report ต้อง Merge หรือ Reject
* งานที่ส่งต่อหลายหน่วยงานต้องติดตามอย่างไร

ประเด็นเหล่านี้จะเก็บไว้ใน Open Questions / Needs Validation

---

## D-09 — Prioritization

ใน Week 05 ทีมเลือกใช้ MoSCoW เพื่อแบ่ง Requirement เป็น:

* **Must** — จำเป็นต่อระบบ
* **Should** — มีประโยชน์สูงแต่สามารถทำภายหลังได้
* **Could** — เป็นความสามารถเพิ่มเติม

การจัด Priority ต้องพิจารณา Value, Risk, Urgency และ Dependency ไม่ใช่เลือกตามความชอบของสมาชิก

---

## D-10 — Baseline Preparation

ก่อนเข้าสู่ Requirement Baseline ทีมตัดสินใจว่าต้องตรวจสอบความสอดคล้องของ:

`Evidence Log`
→ `Requirement Candidates`
→ `Prioritization Rationale`
→ `Requirement Backlog`

โดยเฉพาะ Req ID และ Evidence ID เพื่อป้องกัน Traceability ผิดพลาด

---

# Open Decisions / Pending Decisions

รายการต่อไปนี้ **ยังไม่ถือเป็น Final Decision** เนื่องจากยังต้องมี Evidence เพิ่มเติม

| Pending ID | Issue                             | Related Requirement | Next Action                    |
| ---------- | --------------------------------- | ------------------- | ------------------------------ |
| `PD-01`    | เกณฑ์ใดถือเป็น Urgent             | `FR-CLMRS-03`       | สัมภาษณ์/ยืนยันกับผู้รับผิดชอบ |
| `PD-02`    | ใครมีสิทธิ์ยืนยันการปิดงาน        | `FR-CLMRS-06`       | ยืนยัน Workflow กับเจ้าหน้าที่ |
| `PD-03`    | จัดการ Duplicate Report อย่างไร   | `FR-CLMRS-05`       | เก็บ Evidence เพิ่ม            |
| `PD-04`    | ช่องทาง Notification ที่ต้องการ   | `FR-CLMRS-08`       | สอบถาม Stakeholder             |
| `PD-05`    | รายงาน/KPI ที่ผู้บริหารต้องการ    | `FR-CLMRS-09`       | สัมภาษณ์ผู้ดูแลอาคาร/ผู้บริหาร |
| `PD-06`    | Workflow งานที่ส่งต่อหลายหน่วยงาน | `FR-CLMRS-07`       | ยืนยันกับผู้รับผิดชอบงาน       |

---

# Decision Log Maintenance Rules

1. เพิ่ม Decision ใหม่เมื่อมีการตัดสินใจที่ส่งผลต่อ Scope, Requirement หรือการออกแบบระบบ
2. ไม่บันทึกสิ่งที่เป็นเพียง Task หรือกิจกรรมประจำเป็น Decision
3. ทุก Decision ควรระบุเหตุผลที่ตรวจสอบได้
4. Decision ที่ยังไม่มีข้อมูลเพียงพอให้บันทึกเป็น Pending Decision แทน
5. หาก Decision เปลี่ยน Requirement ต้องอัปเดต Artefact ที่เกี่ยวข้องด้วย
6. ไม่สร้าง Commit Hash หรือ Link ที่ไม่มีอยู่จริง
7. Decision Log ต้องสอดคล้องกับเอกสาร Requirement ล่าสุด

---

# Revision History

| Version | Date       | Change                                                  |
| ------- | ---------- | ------------------------------------------------------- |
| `v0.1`  | 04/08/2026 | เริ่มจัดทำ Decision Log จากงาน Week 01                  |
| `v0.2`  | 13/07/2026 | เพิ่มการตัดสินใจด้าน Stakeholder / Scope                |
| `v0.3`  | 20/07/2026 | เพิ่ม Elicitation Decisions                             |
| `v0.4`  | 27/07/2026 | เพิ่ม Evidence / Requirement / Negotiation Decisions    |
| `v0.5`  | 04/08/2026 | เพิ่ม Prioritization / Backlog / Traceability Decisions |
