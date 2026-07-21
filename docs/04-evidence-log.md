# Week 04 — Evidence Log & Initial Requirement Candidates

> **Team:** Group 02 — Classroom & Laboratory Maintenance Reporting System
>
> **Case:** ระบบแจ้งซ่อมอุปกรณ์ในห้องเรียนและห้องปฏิบัติการ# Week 04 — Evidence Log & Initial Requirement Candidates

> **Team:** Group 02 — Classroom & Laboratory Maintenance Reporting System
>
> **Case:** ระบบแจ้งซ่อมอุปกรณ์ในห้องเรียนและห้องปฏิบัติการ
>
> **Status:** Initial evidence and requirement candidates collected during Week 04.
> **สถานะ:** หลักฐานและ Candidate Requirements เบื้องต้นที่ได้จากการเก็บข้อมูลใน Week 04
>
> **These are not yet approved requirements or an SRS.**
> **ยังไม่ใช่ Requirement ที่ได้รับการยืนยันหรือเอกสาร SRS**
>
> **Week 05 will validate, categorize, and refine these requirements.**
> **Week 05 จะนำหลักฐานมาวิเคราะห์ จัดหมวดหมู่ และปรับปรุง Requirement ให้สมบูรณ์**

---

# 1. Evidence Log

| Evidence ID | Source | Statement / Observation | Type | Related OQ | Initial Interpretation |
|---|---|---|---|---|---|
| E-01 | Student Interview | เมื่อพบอุปกรณ์เสีย ส่วนใหญ่จะแจ้งอาจารย์ผู้สอนหรือเจ้าหน้าที่ด้วยวาจา ทำให้ข้อมูลไม่ถูกบันทึกเป็นระบบ | Observation | OQ-03 | ควรมีระบบกลางสำหรับรับแจ้งปัญหาและลดการแจ้งซ้ำ |
| E-02 | Technician Interview | งานที่กระทบต่อความปลอดภัย หรือทำให้ห้องเรียนใช้งานไม่ได้ จะได้รับการดำเนินการก่อน | Statement | OQ-01 | จำเป็นต้องมีเกณฑ์กำหนดระดับความเร่งด่วนของงาน |
| E-03 | Technician Interview | เมื่อซ่อมเสร็จ เจ้าหน้าที่เป็นผู้บันทึกผล แต่บางกรณีอาจต้องให้อาจารย์หรือผู้แจ้งตรวจสอบก่อนปิดงาน | Statement | OQ-02 | ขั้นตอนการยืนยันการปิดงานยังต้องตรวจสอบเพิ่มเติม |
| E-04 | Student Interview | หลังแจ้งปัญหา ผู้ใช้งานต้องการทราบสถานะงาน แต่ยังไม่แน่ใจว่าควรแจ้งผ่านช่องทางใด | Observation | OQ-04 | ต้องศึกษาช่องทางแจ้งเตือนที่เหมาะสม |
| E-05 | Manager Interview | ผู้บริหารต้องการรายงานจำนวนงานแจ้งซ่อม งานที่ดำเนินการเสร็จ และงานค้าง เพื่อใช้วางแผนงบประมาณ | Statement | OQ-05 | ระบบควรสามารถจัดทำรายงานสรุปได้ |
| E-06 | Technician Interview | หากงานต้องส่งต่อหลายหน่วยงาน การติดตามสถานะทำได้ยาก เพราะไม่มีจุดรวมข้อมูลกลาง | Observation | OQ-06 | ควรมีการติดตามสถานะของงานที่ถูกส่งต่อระหว่างหน่วยงาน |

---

# 2. Initial Requirement Candidates

| ID | Candidate Type | Candidate Requirement | Evidence | Confidence | Open Validation |
|---|---|---|---|---|---|
| RC-F-01 | Functional | ระบบควรสามารถกำหนดระดับความเร่งด่วนของงานแจ้งซ่อมได้ | E-02 | Medium | ต้องยืนยันเกณฑ์ Urgent (OQ-01) |
| RC-F-02 | Functional | ระบบควรให้เจ้าหน้าที่บันทึกผลการซ่อมและรองรับการยืนยันการปิดงาน | E-03 | Medium | ต้องยืนยันผู้รับผิดชอบในการปิดงาน (OQ-02) |
| RC-F-03 | Functional | ระบบควรช่วยลดการแจ้งปัญหาซ้ำ และสามารถเชื่อมโยงรายการที่เกี่ยวข้องได้ | E-01 | Low | ต้องยืนยันแนวทางจัดการรายการแจ้งซ้ำ (OQ-03) |
| RC-F-04 | Functional | ระบบควรแจ้งความคืบหน้าของงานซ่อมให้ผู้ใช้งานทราบ | E-04 | Medium | ต้องยืนยันช่องทางการแจ้งเตือน (OQ-04) |
| RC-F-05 | Functional | ระบบควรจัดทำรายงานและสถิติงานซ่อมสำหรับผู้บริหาร | E-05 | Medium | ต้องยืนยันรูปแบบรายงานที่ต้องการ (OQ-05) |
| RC-F-06 | Functional | ระบบควรติดตามสถานะงานที่ถูกส่งต่อระหว่างหลายหน่วยงานได้ | E-06 | Medium | ต้องยืนยัน Workflow การส่งต่องาน (OQ-06) |

---

# 3. Conflict / Unknown

| ID | Issue | Evidence | Related OQ | Next Question |
|---|---|---|---|---|
| CU-01 | ยังไม่มีข้อสรุปว่าหากมีผู้ใช้งานหลายคนแจ้งปัญหาเดียวกัน ระบบควรรวมรายการเดิมหรือสร้างรายการใหม่ | E-01 | OQ-03 | ใครเป็นผู้ตัดสินใจจัดการรายการแจ้งซ้ำ และควรมีหลักเกณฑ์อย่างไร |

---

# 4. Notes

- Requirement Candidates ทุกข้อยังเป็นข้อเสนอเบื้องต้น (Candidate Requirements)
- หลักฐานที่เก็บได้จะถูกนำไปตรวจสอบและยืนยันเพิ่มเติมใน Week 05
- หากมี Evidence ใหม่ ให้เพิ่ม Evidence ID และปรับระดับ Confidence ตามข้อมูลที่ได้รับ
- หากพบข้อมูลที่ขัดแย้งกัน ให้บันทึกไว้ในส่วน Conflict / Unknown ก่อนสรุปเป็น Requirement

>
> **Status:** Initial evidence and requirement candidates collected during Week 04.
> **สถานะ:** หลักฐานและ Candidate Requirements เบื้องต้นที่ได้จากการเก็บข้อมูลใน Week 04
>
> **These are not yet approved requirements or an SRS.**
> **ยังไม่ใช่ Requirement ที่ได้รับการยืนยันหรือเอกสาร SRS**
>
> **Week 05 will validate, categorize, and refine these requirements.**
> **Week 05 จะนำหลักฐานมาวิเคราะห์ จัดหมวดหมู่ และปรับปรุง Requirement ให้สมบูรณ์**

---

# 1. Evidence Log

| Evidence ID | Source | Statement / Observation | Type | Related Question | Initial Interpretation |
|---|---|---|---|---|---|
| E-01 | Student Interview | เมื่อพบอุปกรณ์เสีย ส่วนใหญ่จะแจ้งอาจารย์ผู้สอน หรือแจ้งเจ้าหน้าที่ด้วยวาจา เพราะไม่ทราบช่องทางอื่น | Observation | Q-01 | ปัจจุบันยังไม่มีช่องทางการแจ้งซ่อมที่เป็นมาตรฐาน |
| E-02 | Teacher Interview | หากผู้แจ้งไม่ระบุห้องหรือรายละเอียดของปัญหา ต้องสอบถามข้อมูลเพิ่มเติมก่อนส่งต่อให้เจ้าหน้าที่ | Observation | Q-02, Q-03 | ข้อมูลไม่ครบทำให้การดำเนินงานล่าช้า |
| E-03 | Technician Interview | ข้อมูลที่จำเป็นสำหรับการรับงาน ได้แก่ อาคาร ห้อง รายละเอียดปัญหา และรูปภาพประกอบ (ถ้ามี) | Statement | Q-03 | ระบบควรเก็บข้อมูลที่จำเป็นสำหรับการแจ้งซ่อม |
| E-04 | Manager Interview | อุปกรณ์ที่ส่งผลกระทบต่อการเรียนการสอน เช่น โปรเจกเตอร์ ระบบไฟฟ้า หรือระบบเครือข่าย ควรได้รับการดำเนินการก่อนงานทั่วไป | Statement | Q-04 | ระบบควรสนับสนุนการจัดลำดับความสำคัญของงาน |
| E-05 | Student Interview | หลังแจ้งซ่อมแล้ว ผู้ใช้งานไม่ทราบว่างานอยู่ในขั้นตอนใด ต้องสอบถามเจ้าหน้าที่หลายครั้ง | Observation | Q-06 | ผู้ใช้งานต้องการติดตามสถานะงานซ่อมได้ |

---

# 2. Initial Requirement Candidates

| ID | Candidate Type | Candidate Requirement | Evidence | Confidence | Open Validation |
|---|---|---|---|---|---|
| RC-F-01 | Functional | ระบบควรให้ผู้ใช้งานแจ้งปัญหาอุปกรณ์หรือห้องเรียนที่ชำรุดได้ | E-01 | High | - |
| RC-F-02 | Functional | ระบบควรบันทึกข้อมูลที่จำเป็นสำหรับการแจ้งซ่อม เช่น อาคาร ห้อง รายละเอียดปัญหา และรูปภาพประกอบ (ถ้ามี) | E-02, E-03 | High | ต้องยืนยันว่าจำเป็นต้องใช้ข้อมูลใดบ้าง |
| RC-F-03 | Functional | ระบบควรสนับสนุนการจัดลำดับความสำคัญของงานซ่อมตามระดับความเร่งด่วน | E-04 | Medium | ต้องยืนยันเกณฑ์การกำหนดระดับความเร่งด่วน |
| RC-F-04 | Functional | ระบบควรให้ผู้ใช้งานสามารถติดตามสถานะของรายการแจ้งซ่อมของตนเองได้ | E-05 | Medium | ต้องยืนยันข้อมูลและสถานะที่ผู้ใช้ต้องการเห็น |
| RC-F-05 | Functional | ระบบควรให้เจ้าหน้าที่บันทึกผลการดำเนินงานและปิดงานซ่อมได้ | Needs Validation | Low | ต้องยืนยันผู้รับผิดชอบในการปิดงานและขั้นตอนการยืนยัน |

---

# 3. Conflict / Unknown

| ID | Issue | Evidence | Next Question |
|---|---|---|---|
| CU-01 | ยังไม่มีข้อสรุปเกี่ยวกับแนวทางการจัดการกรณีมีการแจ้งปัญหาซ้ำของอุปกรณ์หรือห้องเดียวกัน | E-01, E-03 | ระบบควรรวมรายการแจ้งซ่อมเดิมหรือสร้างรายการใหม่ และใครเป็นผู้ตัดสินใจในการจัดการรายการแจ้งซ้ำ |

---

# 4. Notes

- Requirement Candidates ทุกข้อยังเป็นข้อเสนอเบื้องต้น (Candidate Requirements)
- จะต้องเก็บหลักฐานเพิ่มเติมใน Week 04 และตรวจสอบความถูกต้องอีกครั้งใน Week 05
- หากมี Evidence ใหม่ ให้เพิ่ม Evidence ID และปรับระดับ Confidence พร้อมบันทึกเหตุผล
- หากพบข้อมูลที่ขัดแย้งกัน ให้บันทึกไว้ในส่วน Conflict / Unknown ก่อนสรุปเป็น Requirement
