# Week 04 — Evidence Log & Initial Requirement Candidates

> **Team:** Group 02 — Classroom & Laboratory Maintenance Reporting System
>
> **Case:** ระบบแจ้งซ่อมอุปกรณ์ในห้องเรียนและห้องปฏิบัติการ
>
> **Status:** Initial evidence and requirement candidates collected during Week 04.  
> **สถานะ:** หลักฐานและ Candidate Requirements เบื้องต้นที่ได้จากการเก็บข้อมูลใน Week 04
># 04 — Evidence Log: Classroom & Laboratory Maintenance Reporting System

## 1. Source Summary

| Field | Value |
|---|---|
| Case | Classroom & Laboratory Maintenance Reporting System |
| AI role(s) used | Student / Teacher, Technician, Building Manager |
| Source files | Week03 Elicitation Plan, Week03 Interview Guide |
| Conversation excerpt | `../evidence/week-04/ai-conversation-excerpt.md` |

---

## 2. Evidence Log

| E-ID | Source / Role | Evidence quote or summary | Tag | Interpreted Need | Related RC | Follow-up / Unknown |
|---|---|---|---|---|---|---|
| E-01 | AI: Student | เมื่อพบอุปกรณ์เสีย นักศึกษาไม่ทราบช่องทางแจ้งที่ถูกต้อง จึงแจ้งอาจารย์หรือเจ้าหน้าที่ด้วยวาจา | NEED | ผู้ใช้งานต้องมีช่องทางแจ้งซ่อมที่เป็นมาตรฐาน | RC-F-03 | ต้องยืนยันข้อมูลขั้นต่ำที่ต้องใช้ในการแจ้งซ่อม |
| E-02 | AI: Teacher | หากอุปกรณ์เสียระหว่างการสอน ต้องการให้แก้ไขโดยเร็ว เพราะส่งผลกระทบต่อการเรียน | NEED | ระบบควรสนับสนุนการจัดลำดับงานเร่งด่วน | RC-F-01 | ต้องยืนยันเกณฑ์การกำหนด Urgent |
| E-03 | AI: Technician | ก่อนรับงานต้องทราบอาคาร ห้อง รายละเอียดปัญหา และผู้แจ้ง หากข้อมูลไม่ครบต้องสอบถามเพิ่มเติม | CONSTRAINT | ระบบต้องบังคับข้อมูลขั้นต่ำก่อนส่งคำขอ | RC-F-02 | ต้องยืนยันข้อมูลที่จำเป็นทั้งหมด |
| E-04 | AI: Technician | หากมีผู้แจ้งปัญหาเดียวกันหลายครั้ง เจ้าหน้าที่ต้องตรวจสอบเองว่าเป็นงานเดิมหรือไม่ | UNKNOWN | ระบบควรช่วยตรวจสอบหรือเชื่อมโยงรายการแจ้งซ้ำ | RC-F-03 | ต้องยืนยันแนวทางจัดการรายการแจ้งซ้ำ |
| E-05 | AI: Student / Teacher | หลังแจ้งซ่อม ผู้แจ้งไม่ทราบว่างานอยู่ในขั้นตอนใด ต้องสอบถามเจ้าหน้าที่หลายครั้ง | NEED | ผู้แจ้งควรสามารถติดตามสถานะงานได้ | RC-F-04 | ต้องยืนยันข้อมูลและสถานะที่ต้องการเห็น |
| E-06 | AI: Building Manager | ต้องการรายงานจำนวนงานซ่อม งานค้าง งานเร่งด่วน และเวลาที่ใช้ในการซ่อม เพื่อใช้วางแผนงบประมาณ | NEED | ระบบควรจัดทำรายงานสำหรับผู้บริหาร | RC-F-05 | ต้องยืนยันรูปแบบรายงานและ KPI |
| E-07 | AI: Technician | เมื่อส่งต่องานไปหลายหน่วยงาน การติดตามสถานะทำได้ยาก เพราะไม่มีระบบกลาง | CONSTRAINT | ระบบควรติดตามสถานะการส่งต่องานได้ | RC-F-06 | ต้องยืนยัน Workflow การส่งต่องาน |

---

## 3. How the Team Derived Needs

| Evidence | ทำไมถือเป็น Need/Constraint | Need ที่ได้ |
|---|---|---|
| E-01 | ผู้ใช้ไม่ทราบช่องทางแจ้งซ่อมที่เป็นมาตรฐาน | N-01 ผู้ใช้งานต้องมีช่องทางแจ้งซ่อมที่ชัดเจน |
| E-02 | การเรียนการสอนได้รับผลกระทบโดยตรง | N-02 ระบบต้องรองรับการจัดลำดับความเร่งด่วนของงาน |
| E-03 | เจ้าหน้าที่ไม่สามารถเริ่มงานได้หากข้อมูลไม่ครบ | N-03 ระบบต้องเก็บข้อมูลขั้นต่ำก่อนรับแจ้ง |
| E-04 | การแจ้งซ้ำทำให้เกิดงานซ้ำและเสียเวลา | N-04 ระบบต้องช่วยจัดการรายการแจ้งปัญหาซ้ำ |
| E-05 | ผู้แจ้งไม่ทราบความคืบหน้าของงาน | N-05 ผู้แจ้งต้องสามารถติดตามสถานะงานได้ |
| E-06 | ผู้บริหารใช้ข้อมูลในการวางแผน | N-06 ผู้บริหารต้องเห็นรายงานและสถิติการซ่อม |
| E-07 | การส่งต่องานหลายหน่วยงานติดตามได้ยาก | N-07 ระบบต้องติดตามสถานะการส่งต่องานได้ |

---

## 4. Need Summary

| Need ID | Need statement | Based on E-ID(s) | Notes |
|---|---|---|---|
| N-01 | Users need a standard channel for reporting maintenance issues. | E-01 | ลดการแจ้งผ่านหลายช่องทาง |
| N-02 | Teachers and technicians need urgent issues to be prioritized. | E-02 | ต้องกำหนดเกณฑ์ Urgent |
| N-03 | Technicians need complete maintenance request information before accepting a job. | E-03 | ใช้กำหนดข้อมูลขั้นต่ำของแบบฟอร์ม |
| N-04 | Technicians need duplicate maintenance reports to be identified. | E-04 | ยังต้องยืนยันวิธีจัดการ |
| N-05 | Students and teachers need to track maintenance request status. | E-05 | ต้องกำหนดสถานะที่แสดง |
| N-06 | Building managers need maintenance reports and statistics. | E-06 | ใช้สำหรับการวางแผนและตัดสินใจ |
| N-07 | Technicians need to track jobs transferred between departments. | E-07 | เกี่ยวข้องกับ Workflow การส่งต่องาน |

---

## 5. Unknowns / Follow-up for Week 05

| OQ-ID | Question | Why it matters | Who/what can verify |
|---|---|---|---|
| OQ-01 | เกณฑ์ใดใช้กำหนดว่างานเป็นงานเร่งด่วน (Urgent)? | ใช้กำหนด Priority ของงานซ่อม | Technician / Building Manager |
| OQ-02 | ใครเป็นผู้รับผิดชอบและผู้ยืนยันการปิดงานซ่อม? | ใช้ออกแบบ Workflow การปิดงาน | Technician / Building Manager |
| OQ-03 | หากพบการแจ้งปัญหาซ้ำ ระบบควรจัดการอย่างไร? | ลดงานซ้ำและเพิ่มประสิทธิภาพ | Technician |
| OQ-04 | ผู้ใช้งานต้องการรับการแจ้งเตือนผ่านช่องทางใด? | ใช้ออกแบบการติดตามสถานะ | Student / Teacher |
| OQ-05 | ผู้บริหารต้องการรายงานหรือสถิติประเภทใดบ้าง? | ใช้ออกแบบ Dashboard และรายงาน | Building Manager |
| OQ-06 | กรณีส่งต่องานไปหลายหน่วยงาน ควรติดตามสถานะอย่างไร? | รองรับ Workflow การประสานงาน | Technician / Building Manager |
> **These are not yet approved requirements or an SRS.**  
> **ยังไม่ใช่ Requirement ที่ได้รับการยืนยันหรือเอกสาร SRS**
>
> **Week 05 will validate, categorize, and refine these requirements.**  
> **Week 05 จะนำหลักฐานมาวิเคราะห์ จัดหมวดหมู่ และปรับปรุง Requirement ให้สมบูรณ์**

---

# 1. Evidence Log

| Evidence ID | Source | Statement / Observation | Type | Related OQ | Initial Interpretation |
|---|---|---|---|---|---|
| E-01 | Student Interview | เมื่อพบอุปกรณ์เสีย ส่วนใหญ่จะแจ้งอาจารย์ผู้สอนหรือเจ้าหน้าที่ด้วยวาจา เพราะไม่ทราบช่องทางการแจ้งที่เป็นทางการ | Observation | OQ-03 | ควรมีระบบกลางสำหรับรับแจ้งปัญหาและช่วยลดการแจ้งซ้ำ |
| E-02 | Teacher Interview | หากอุปกรณ์เสียระหว่างการเรียนการสอน เช่น โปรเจกเตอร์หรือคอมพิวเตอร์ อาจารย์ต้องรีบแจ้งเจ้าหน้าที่ทันที และบางครั้งต้องเปลี่ยนห้องเรียน | Observation | OQ-01 | งานที่ส่งผลกระทบต่อการเรียนการสอนควรได้รับการจัดลำดับความสำคัญ |
| E-03 | Technician Interview | เมื่อได้รับแจ้งซ่อม เจ้าหน้าที่ต้องตรวจสอบข้อมูล เช่น อาคาร ห้อง รายละเอียดปัญหา และบันทึกผลการซ่อม ก่อนปิดงาน | Statement | OQ-02 | ระบบควรรองรับการบันทึกผลการซ่อมและการปิดงาน |
| E-04 | Student Interview | หลังแจ้งซ่อมแล้ว ผู้ใช้งานไม่ทราบว่างานอยู่ในขั้นตอนใด จึงต้องสอบถามเจ้าหน้าที่หลายครั้ง | Observation | OQ-04 | ผู้ใช้งานต้องการติดตามสถานะของงานซ่อม |
| E-05 | Teacher Interview | อาจารย์ต้องการทราบความคืบหน้าของงานซ่อม เพื่อวางแผนการเรียนการสอน หากซ่อมไม่ทันจะได้เตรียมห้องหรืออุปกรณ์สำรอง | Statement | OQ-04 | ผู้สอนต้องสามารถติดตามสถานะงานซ่อมได้ |
| E-06 | Manager Interview | ผู้บริหารต้องการรายงานจำนวนงานแจ้งซ่อม งานที่ดำเนินการเสร็จ งานค้าง และงานเร่งด่วน เพื่อใช้วางแผนและจัดสรรงบประมาณ | Statement | OQ-05 | ระบบควรจัดทำรายงานและสถิติสำหรับผู้บริหาร |
| E-07 | Technician Interview | หากงานต้องส่งต่อหลายหน่วยงาน การติดตามสถานะทำได้ยาก เพราะไม่มีจุดรวมข้อมูลกลาง | Observation | OQ-06 | ระบบควรติดตามสถานะของงานที่ถูกส่งต่อระหว่างหลายหน่วยงานได้ |

---

# 2. Initial Requirement Candidates

| ID | Candidate Type | Candidate Requirement | Evidence | Confidence | Open Validation |
|---|---|---|---|---|---|
| RC-F-01 | Functional | ระบบควรสามารถกำหนดระดับความเร่งด่วนของงานแจ้งซ่อมได้ | E-02 | Medium | ต้องยืนยันเกณฑ์การกำหนดงานเร่งด่วน (OQ-01) |
| RC-F-02 | Functional | ระบบควรให้เจ้าหน้าที่บันทึกผลการซ่อม และรองรับการยืนยันการปิดงาน | E-03 | Medium | ต้องยืนยันผู้รับผิดชอบในการปิดงาน (OQ-02) |
| RC-F-03 | Functional | ระบบควรช่วยลดการแจ้งปัญหาซ้ำ และสามารถเชื่อมโยงรายการแจ้งซ่อมที่เกี่ยวข้องได้ | E-01 | Low | ต้องยืนยันแนวทางจัดการรายการแจ้งซ้ำ (OQ-03) |
| RC-F-04 | Functional | ระบบควรให้ผู้แจ้งซ่อม เช่น นักศึกษาและอาจารย์ผู้สอน สามารถติดตามสถานะของรายการแจ้งซ่อมได้ | E-04, E-05 | Medium | ต้องยืนยันข้อมูลและช่องทางที่ต้องการ (OQ-04) |
| RC-F-05 | Functional | ระบบควรจัดทำรายงานและสถิติงานซ่อมสำหรับผู้ดูแลอาคารหรือผู้บริหาร | E-06 | Medium | ต้องยืนยันรูปแบบรายงานและตัวชี้วัดที่ต้องการ (OQ-05) |
| RC-F-06 | Functional | ระบบควรติดตามสถานะของงานซ่อมที่ถูกส่งต่อระหว่างหลายหน่วยงานได้ | E-07 | Medium | ต้องยืนยัน Workflow การส่งต่องาน (OQ-06) |

---

# 3. Conflict / Unknown

| ID | Issue | Evidence | Related OQ | Next Question |
|---|---|---|---|---|
| CU-01 | ยังไม่มีข้อสรุปว่าหากมีผู้ใช้งานหลายคนแจ้งปัญหาเดียวกัน ระบบควรรวมรายการแจ้งเดิมหรือสร้างรายการใหม่ | E-01 | OQ-03 | ระบบควรจัดการรายการแจ้งปัญหาซ้ำอย่างไร และใครเป็นผู้ตัดสินใจรวมหรือแยกรายการแจ้งซ่อม |

---

# 4. Notes

- Requirement Candidates ทุกข้อยังเป็นข้อเสนอเบื้องต้น (Candidate Requirements)
- จะต้องเก็บหลักฐานเพิ่มเติมและตรวจสอบความถูกต้องอีกครั้งใน Week 05
- หากมี Evidence ใหม่ ให้เพิ่ม Evidence ID และปรับระดับ Confidence ตามหลักฐานที่ได้รับ
- หากพบข้อมูลที่ขัดแย้งกัน ให้บันทึกไว้ในส่วน **Conflict / Unknown** ก่อนสรุปเป็น Requirement
