# Week 04 — Evidence Log & Initial Requirement Candidates

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
