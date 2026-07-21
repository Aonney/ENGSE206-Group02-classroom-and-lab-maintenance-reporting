# 04 — Requirement Candidates: Classroom & Laboratory Maintenance Reporting System

## 1. How We Turned Evidence into Requirement Candidates

หลักคิดของทีม:

1. เริ่มจากหลักฐาน (Evidence) ที่มี Evidence ID (E-ID)
2. วิเคราะห์ความต้องการ (Need) จากปัญหาหรือข้อจำกัดที่ Stakeholder ให้ข้อมูล
3. แปลง Need เป็น Requirement Candidate ของระบบ
4. ระบุสถานะเป็น `Candidate` หรือ `Needs Validation`
5. หากยังไม่มีหลักฐานเพียงพอ จะบันทึกไว้เป็น Follow-up สำหรับ Week 05

```mermaid
flowchart LR
    E["E-01: ผู้ใช้แจ้งซ่อมผ่านหลายช่องทาง"] --> N["N-01: ต้องมีช่องทางแจ้งซ่อมที่เป็นมาตรฐาน"]
    N --> R["RC-01: ระบบรองรับการแจ้งซ่อมผ่านระบบออนไลน์"]
```

---

## 2. Requirement Candidate Table

| RC-ID | Requirement Candidate | Stakeholder / Need | Evidence E-ID(s) | Status | Follow-up |
|---|---|---|---|---|---|
| RC-01 | The system should allow students and instructors to submit maintenance requests through a standardized reporting system. | Student, Teacher / N-01 | E-01 | Candidate | ตรวจสอบข้อมูลที่จำเป็นในแบบฟอร์ม |
| RC-02 | The system should require users to provide essential maintenance information such as building, room, problem description, and supporting photo (if available). | Technician / N-02 | E-02, E-03 | Candidate | ยืนยันว่าข้อมูลใดเป็นข้อมูลบังคับ |
| RC-03 | The system should support prioritizing maintenance requests based on urgency criteria. | Technician, Manager / N-03 | E-04 | Needs Validation | ยืนยันเกณฑ์การกำหนดงาน Urgent (OQ-01) |
| RC-04 | The system should allow users to track the status of their maintenance requests. | Student, Teacher / N-04 | E-05 | Candidate | ยืนยันสถานะที่ผู้ใช้ต้องการเห็น (OQ-04) |
| RC-05 | The system should allow technicians to record repair results and close maintenance requests. | Technician / N-05 | E-03 | Needs Validation | ยืนยันผู้รับผิดชอบการปิดงาน (OQ-02) |
| RC-06 | The system should support handling duplicate maintenance reports for the same problem. | Technician / N-06 | E-01, E-03 | Needs Validation | ยืนยันแนวทางจัดการรายการแจ้งซ้ำ (OQ-03) |
| RC-07 | The system should support tracking maintenance requests that are transferred between multiple departments. | Technician, Manager / N-07 | Needs Validation | Needs Validation | ยืนยัน Workflow การส่งต่องาน (OQ-06) |
| RC-08 | The system should provide maintenance reports and statistics to support management decision-making. | Manager / N-08 | Needs Validation | Needs Validation | ยืนยันประเภทของรายงานที่ต้องการ (OQ-05) |

---

## 3. Why These Are Candidates, Not Final Requirements

| RC | เหตุผลที่ยังไม่เป็น Final Requirement |
|---|---|
| RC-03 | ยังไม่มีหลักฐานยืนยันเกณฑ์การกำหนดงานเร่งด่วน (Urgent) |
| RC-05 | ยังไม่ทราบผู้รับผิดชอบในการยืนยันและปิดงานซ่อม |
| RC-06 | ยังไม่มีข้อสรุปเกี่ยวกับการจัดการกรณีแจ้งปัญหาซ้ำ |
| RC-07 | ยังไม่ทราบขั้นตอนการติดตามงานที่ส่งต่อหลายหน่วยงาน |
| RC-08 | ยังไม่ยืนยันว่าผู้บริหารต้องการรายงานหรือ KPI ประเภทใด |

---

## 4. Candidate to Week 05 Backlog Handoff

| Week 04 RC | Move to Week 05? | Reason |
|---|---|---|
| RC-01 | Yes | เป็นความสามารถหลักของระบบ |
| RC-02 | Yes | มีหลักฐานสนับสนุนจากหลาย Stakeholders |
| RC-03 | Yes, revise after validation | ต้องยืนยันเกณฑ์ Urgent |
| RC-04 | Yes | สอดคล้องกับ Pain Point ของผู้ใช้งาน |
| RC-05 | Revise | ต้องยืนยัน Workflow การปิดงาน |
| RC-06 | Revise | ต้องหาหลักฐานเกี่ยวกับการแจ้งปัญหาซ้ำ |
| RC-07 | Revise | ต้องยืนยันการส่งต่องานหลายหน่วยงาน |
| RC-08 | Revise | ต้องสอบถามผู้บริหารเพิ่มเติม |

---

## 5. Student Takeaway

Requirement Candidate ที่ดีควรสามารถอธิบายได้ว่า

- อ้างอิงหลักฐาน (Evidence) ใด
- ตอบสนอง Need ของ Stakeholder ใด
- ยังมีข้อมูลใดที่ต้องตรวจสอบเพิ่มเติม
- จะนำไปตรวจสอบและปรับปรุงใน Week 05 อย่างไร
