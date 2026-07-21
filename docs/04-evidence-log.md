# 04 — Evidence Log: Classroom & Laboratory Maintenance Reporting System

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
