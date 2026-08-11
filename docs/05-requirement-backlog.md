# 05 — Requirement Backlog v0.1: Classroom & Laboratory Maintenance Reporting System

> **Case:** Classroom & Laboratory Maintenance Reporting System (CLMRS)
>
> **Source:** Week 04 Evidence Log, Need Summary และ Initial Requirement Candidates
>
> **Status:** Initial Requirement Backlog
>
> **สถานะ:** Backlog ความต้องการเบื้องต้นจากหลักฐานใน Week 04
>
> **Goal:** จัดประเภท จัดลำดับ และแยก Requirement ที่พร้อมนำไปใช้ต่อใน Week 06 ออกจากรายการที่ยังต้องตรวจสอบเพิ่มเติม

---

# 1. Project Metadata

| Field | Value |
|---|---|
| Course / Week | ENGSE206 / Week 05 |
| Team | Group 02 |
| Case | Classroom & Laboratory Maintenance Reporting System |
| Case No. | No.02 |
| Backlog Version | v0.1 |
| Status | Draft / Initial |
| Date | 2026-08-11 |

---

# 2. Prioritization Method

ทีมใช้แนวคิด **MoSCoW** เพื่อจัดลำดับความสำคัญของ Requirement โดยพิจารณาจาก 4 มิติ

| Dimension | วิธีใช้กับระบบ |
|---|---|
| **Value** | Requirement ช่วยให้ผู้ใช้งานหรือเจ้าหน้าที่ทำงานหลักได้ดีขึ้นหรือไม่ |
| **Risk** | หากไม่มี Requirement นี้ จะทำให้ข้อมูลสูญหาย งานล่าช้า หรือเกิดงานซ้ำหรือไม่ |
| **Urgency** | จำเป็นต่อการทำงานของระบบในรุ่นแรกหรือสามารถพัฒนาในภายหลังได้ |
| **Dependency** | Requirement นี้ต้องรอการยืนยันจาก Stakeholder, Policy หรือข้อมูลอื่นหรือไม่ |

### MoSCoW

- **Must** — จำเป็นต่อระบบรุ่นแรก
- **Should** — มีความสำคัญสูง แต่สามารถพัฒนาหลัง Must ได้
- **Could** — มีประโยชน์ แต่ไม่จำเป็นสำหรับรุ่นแรก
- **Won't yet** — ยังไม่ทำในรอบนี้ เนื่องจากข้อมูลหรือหลักฐานยังไม่เพียงพอ

---

# 3. Requirement Backlog v0.1

| Req ID | Source RC | Evidence / Need Trace | Requirement Statement | Type | Priority | Rationale | Status | Open Question | Week06 Use |
|---|---|---|---|---|---|---|---|---|---|
| **FR-CLMRS-01** | RC-F-01 | E-01 → N-01 | ระบบต้องให้ผู้ใช้งานสามารถแจ้งปัญหาอุปกรณ์หรือห้องเรียน/ห้องปฏิบัติการที่ชำรุดผ่านช่องทางมาตรฐานของระบบได้ | Functional | **Must** | เป็นความสามารถหลักของระบบและช่วยลดการแจ้งปัญหาผ่านหลายช่องทาง | Ready for Week06 | ข้อมูลขั้นต่ำที่ต้องกรอกมีอะไรบ้าง | User Story + Use Case |
| **FR-CLMRS-02** | RC-F-02 | E-02, E-03 → N-03 | ระบบต้องให้ผู้แจ้งบันทึกข้อมูลที่จำเป็น เช่น อาคาร ห้อง รายละเอียดปัญหา และข้อมูลประกอบที่เกี่ยวข้องก่อนส่งคำขอ | Functional | **Must** | ข้อมูลไม่ครบทำให้เจ้าหน้าที่ต้องสอบถามเพิ่มเติมและทำให้งานล่าช้า | Needs Follow-up | ต้องยืนยัน Required Fields กับเจ้าหน้าที่เทคนิค | Use Case + Acceptance Criteria |
| **FR-CLMRS-03** | RC-F-03 | E-04 → N-02 | ระบบต้องสนับสนุนการจัดลำดับความสำคัญของงานซ่อมตามระดับความเร่งด่วนที่กำหนด | Functional | **Must** | งานที่กระทบต่อการเรียนการสอนควรได้รับการจัดลำดับอย่างเหมาะสม | Needs Follow-up | เกณฑ์ใดใช้กำหนดงาน Urgent และใครเป็นผู้กำหนด | Use Case + Business Rule |
| **FR-CLMRS-04** | RC-F-04 | E-05 → N-05 | ระบบต้องให้ผู้ใช้งานสามารถตรวจสอบสถานะของรายการแจ้งซ่อมของตนเองได้ | Functional | **Must** | ลดปัญหาผู้ใช้งานต้องสอบถามเจ้าหน้าที่หลายครั้ง | Ready for Week06 | ต้องยืนยันสถานะที่ผู้ใช้งานต้องเห็น | User Story + Use Case |
| **FR-CLMRS-05** | RC-F-05 | OQ-02 → N-04 | ระบบควรช่วยให้เจ้าหน้าที่สามารถตรวจสอบและจัดการรายการแจ้งปัญหาที่ซ้ำกันได้ | Functional | **Should** | ช่วยลดงานซ้ำและป้องกันการดำเนินการกับปัญหาเดียวกันหลายครั้ง | Needs Follow-up | หากพบรายการซ้ำควรรวม เชื่อม หรือปิดรายการอย่างไร | Alternate Flow |
| **FR-CLMRS-06** | RC-F-06 | OQ-02 → N-02 | ระบบควรให้เจ้าหน้าที่บันทึกผลการดำเนินงานและปิดงานซ่อม โดยมีผู้รับผิดชอบหรือผู้ยืนยันตาม Workflow ที่กำหนด | Functional + Business Rule | **Should** | จำเป็นต่อการติดตามวงจรงานซ่อมตั้งแต่รับงานจนปิดงาน | Needs Follow-up | ใครเป็นผู้ยืนยันการปิดงาน | Use Case + Business Rule |
| **FR-CLMRS-07** | RC-F-07 | OQ-06 → N-07 | ระบบควรให้เจ้าหน้าที่สามารถติดตามสถานะของงานที่ถูกส่งต่อระหว่างหน่วยงานได้ | Functional | **Should** | รองรับกรณีที่งานไม่สามารถดำเนินการโดยหน่วยงานเดียว | Needs Follow-up | เมื่อส่งต่อแล้วใครเป็นผู้รับผิดชอบหลักและใครเป็นผู้ปิดงาน | Use Case Extension |
| **FR-CLMRS-08** | OQ-04 | OQ-04 → N-05 | ระบบควรแจ้งให้ผู้ใช้งานทราบเมื่อสถานะของงานซ่อมมีการเปลี่ยนแปลงตามช่องทางที่ได้รับการยืนยัน | Functional | **Could** | ช่วยให้ผู้ใช้งานติดตามงานได้สะดวกขึ้น แต่ช่องทางและช่วงเวลายังไม่ยืนยัน | Needs Follow-up | ใช้ช่องทางใด และควรแจ้งในสถานะใดบ้าง | Event / Notification Rule |
| **FR-CLMRS-09** | OQ-05 | OQ-05 → N-06 | ระบบควรสนับสนุนรายงานและสถิติพื้นฐานของงานซ่อมสำหรับผู้ดูแลอาคารหรือผู้บริหาร | Functional | **Should** | ช่วยในการวางแผนและติดตามภาพรวมของงานซ่อม | Needs Follow-up | ผู้บริหารต้องการรายงานและตัวชี้วัดใด | Report Use Case |
| **NFR-CLMRS-01** | Project Scope / Access Control | Stakeholder & Context Analysis | ระบบต้องควบคุมสิทธิ์การเข้าถึงข้อมูลตามบทบาทของผู้ใช้งาน เช่น นักศึกษา อาจารย์ เจ้าหน้าที่เทคนิค และผู้ดูแลอาคาร/ผู้บริหาร | NFR / Constraint | **Must** | ข้อมูลและความสามารถของแต่ละบทบาทไม่ควรเข้าถึงได้เหมือนกันทั้งหมด | Needs Validation | ต้องยืนยัน Role และ Permission Matrix | Quality Scenario + Access Rule |

---

# 4. Requirement Traceability Summary

| Requirement | Evidence | Need | Open Question |
|---|---|---|---|
| FR-CLMRS-01 | E-01 | N-01 | - |
| FR-CLMRS-02 | E-02, E-03 | N-03 | Required Fields |
| FR-CLMRS-03 | E-04 | N-02 | OQ-01 |
| FR-CLMRS-04 | E-05 | N-05 | Status ที่ต้องแสดง |
| FR-CLMRS-05 | OQ-03 | N-04 | วิธีจัดการรายการซ้ำ |
| FR-CLMRS-06 | OQ-02 | N-02 | ผู้ยืนยันการปิดงาน |
| FR-CLMRS-07 | OQ-06 | N-07 | ผู้รับผิดชอบหลังส่งต่อ |
| FR-CLMRS-08 | OQ-04 | N-05 | ช่องทางแจ้งเตือน |
| FR-CLMRS-09 | OQ-05 | N-06 | รายงาน / KPI |
| NFR-CLMRS-01 | Stakeholder / Context | Access Control | Role / Permission |

---

# 5. Priority Summary

| Priority | Count | Requirement IDs | เหตุผลรวม |
|---|---:|---|---|
| **Must** | 4 | FR-CLMRS-01, FR-CLMRS-02, FR-CLMRS-03, FR-CLMRS-04, NFR-CLMRS-01 | เป็นแกนหลักของการแจ้งและติดตามงานซ่อม |
| **Should** | 4 | FR-CLMRS-05, FR-CLMRS-06, FR-CLMRS-07, FR-CLMRS-09 | มีคุณค่าสูง แต่ยังต้องยืนยัน Workflow หรือข้อมูลเพิ่มเติม |
| **Could** | 1 | FR-CLMRS-08 | มีประโยชน์ แต่ช่องทางแจ้งเตือนยังไม่ยืนยัน |
| **Won't yet** | 0 | - | ยังไม่มี Requirement ที่ถูกตัดออกทั้งหมดในรอบนี้ |

> **หมายเหตุ:** NFR-CLMRS-01 ถูกนับเป็น Must แม้ Priority Summary จะมี 5 รายการในกลุ่ม Must เนื่องจากเป็นข้อกำหนดด้านสิทธิ์การเข้าถึงที่สำคัญต่อระบบ

---

# 6. Open Questions ที่ต้องติดตาม

| OQ-ID | Open Question | Related Requirement | Priority |
|---|---|---|---|
| **OQ-01** | เกณฑ์ใดใช้กำหนดว่างานเป็นงานเร่งด่วน (Urgent)? | FR-CLMRS-03 | High |
| **OQ-02** | ใครเป็นผู้รับผิดชอบและผู้ยืนยันการปิดงานซ่อม? | FR-CLMRS-06 | High |
| **OQ-03** | หากพบการแจ้งปัญหาซ้ำ ระบบควรจัดการอย่างไร? | FR-CLMRS-05 | High |
| **OQ-04** | ผู้ใช้งานต้องการรับการแจ้งเตือนผ่านช่องทางใด? | FR-CLMRS-08 | Medium |
| **OQ-05** | ผู้บริหารต้องการรายงานหรือสถิติประเภทใดบ้าง? | FR-CLMRS-09 | Medium |
| **OQ-06** | กรณีส่งต่องานไปหลายหน่วยงาน ควรติดตามสถานะอย่างไร? | FR-CLMRS-07 | Medium |

> **หมายเหตุ:** OQ-04 ยังเป็นคำถามเปิด จึงยังไม่ได้กำหนดช่องทางเฉพาะ เช่น LINE หรือช่องทางอื่น

---

# 7. Conflict / Unknown

## CU-01 — การแจ้งปัญหาซ้ำ

ยังไม่มีหลักฐานเพียงพอที่จะสรุปว่าระบบควรจัดการรายการแจ้งปัญหาซ้ำด้วยวิธีใด

### สถานการณ์ตัวอย่าง

นักศึกษาหลายคนพบว่าโปรเจกเตอร์ในห้องเดียวกันเสีย และมีการแจ้งปัญหาเดียวกันหลายครั้ง

ยังไม่ทราบว่า:

- ระบบควรรวมรายการแจ้งซ่อมเข้าด้วยกันหรือไม่
- ระบบควรเชื่อมรายการใหม่กับรายการเดิมหรือไม่
- ควรสร้างรายการใหม่แต่ระบุว่าเป็นรายการซ้ำหรือไม่
- ใครเป็นผู้ตัดสินใจว่ารายการใดเป็นรายการเดียวกัน

**Related:** OQ-03 / FR-CLMRS-05

**Status:** Needs Validation

---

## CU-02 — เกณฑ์ Urgent

ยังไม่มีหลักฐานเพียงพอที่จะกำหนดเกณฑ์ตายตัวว่าเหตุการณ์ใดเป็นงานเร่งด่วน

ตัวอย่างปัญหาที่ต้องตรวจสอบ:

- อุปกรณ์ที่กระทบต่อการเรียนการสอน
- ระบบไฟฟ้าหรืออุปกรณ์ที่อาจมีความเสี่ยง
- ปัญหาที่ทำให้ไม่สามารถใช้งานห้องได้
- ปัญหาที่สามารถรอการซ่อมตามลำดับปกติได้

**Related:** OQ-01 / FR-CLMRS-03

**Status:** Needs Validation

---

# 8. Ready / Follow-up / Hold

| Status | Requirement IDs | สิ่งที่ต้องทำต่อ |
|---|---|---|
| **Ready for Week06** | FR-CLMRS-01, FR-CLMRS-04 | เริ่มทำ User Story / Use Case |
| **Needs Follow-up** | FR-CLMRS-02, FR-CLMRS-03, FR-CLMRS-05, FR-CLMRS-06, FR-CLMRS-07, FR-CLMRS-08, FR-CLMRS-09, NFR-CLMRS-01 | เก็บ Evidence เพิ่มและยืนยัน Open Questions |
| **Hold** | - | ยังไม่มี Requirement ที่ต้องหยุดทั้งหมด |
| **Issue / Unknown** | CU-01, CU-02 | ห้ามนำไปเขียนเป็น Final Requirement จนกว่าจะมี Evidence เพิ่ม |

---

# 9. Week06 Handoff

Requirement ที่พร้อมนำไปทำงานต่อใน Week06:

| Week06 Artefact | Requirement ที่ใช้ |
|---|---|
| **User Story** | FR-CLMRS-01, FR-CLMRS-04 |
| **Main Use Case** | FR-CLMRS-01 — แจ้งปัญหา |
| **Status Tracking Use Case** | FR-CLMRS-04 — ติดตามสถานะ |
| **Acceptance Criteria** | FR-CLMRS-02 หลังยืนยัน Required Fields |
| **Business Rule** | FR-CLMRS-03 หลังยืนยันเกณฑ์ Urgent |
| **Alternate Flow** | FR-CLMRS-05 — การแจ้งปัญหาซ้ำ |
| **Use Case Extension** | FR-CLMRS-07 — การส่งต่องาน |
| **Report Use Case** | FR-CLMRS-09 หลังยืนยันข้อมูลที่ผู้บริหารต้องการ |
| **Quality Scenario** | NFR-CLMRS-01 — Role / Access Control |

---

# 10. Review Checklist

- [x] ทุก Requirement มี Source หรือ Evidence ที่เกี่ยวข้อง
- [x] ทุก Requirement เชื่อมโยงกับ User Need หรือ Open Question
- [x] แยก Functional / Non-functional / Business Rule / Issue แล้ว
- [x] Priority มีเหตุผลจาก Value, Risk, Urgency และ Dependency
- [x] Open Questions ถูกแยกออกจาก Final Requirements
- [x] การแจ้งปัญหาซ้ำยังถูกเก็บเป็นประเด็นที่ต้องตรวจสอบ
- [x] เกณฑ์ Urgent ยังไม่ถูกกำหนดเองโดยทีม
- [x] ช่องทางการแจ้งเตือนยังไม่กำหนดเป็น LINE หรือช่องทางใดโดยไม่มี Evidence
- [x] Requirement ที่พร้อมสามารถนำไปสร้าง User Story / Use Case ใน Week06 ได้

---

# 11. Week05 Summary

จาก Evidence และ Need ที่เก็บใน Week 04 ทีมสามารถจัดทำ Requirement Backlog เบื้องต้นได้

### Core Requirements

1. แจ้งปัญหาผ่านช่องทางมาตรฐาน
2. บันทึกข้อมูลการแจ้งซ่อมที่จำเป็น
3. จัดลำดับความสำคัญของงาน
4. ติดตามสถานะงานซ่อม
5. จัดการรายการแจ้งปัญหาซ้ำ
6. ปิดงานและบันทึกผลการดำเนินงาน
7. ติดตามงานที่ส่งต่อ
8. สนับสนุนรายงานสำหรับผู้บริหาร

### สิ่งที่ยังต้องตรวจสอบ

- เกณฑ์ Urgent
- ผู้ยืนยันการปิดงาน
- วิธีจัดการแจ้งปัญหาซ้ำ
- ช่องทางและช่วงเวลาการแจ้งเตือน
- รายงานที่ผู้บริหารต้องการ
- Workflow เมื่อส่งต่องานหลายหน่วยงาน

> **หลักสำคัญ:** Requirement ที่ยังไม่มี Evidence เพียงพอจะยังคงเป็น `Needs Follow-up` หรือ `Issue / Unknown` และจะไม่ถูกยกระดับเป็น Final Requirement จนกว่าจะมีหลักฐานสนับสนุน
