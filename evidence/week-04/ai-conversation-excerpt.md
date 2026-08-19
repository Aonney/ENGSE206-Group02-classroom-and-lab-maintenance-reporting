# Week 04 — AI Conversation Excerpt

## Session Information

| Field | Value |
|---|---|
| Date | 04/08/2026 |
| Case | Classroom & Laboratory Maintenance Reporting System (CLMRS) |
| AI role | Student, Teacher, Technician, Building Manager |
| Team interviewer(s) | Interview ENGSE206 — Group 02 |
| Source used | Interview Transcripts (Student, Teacher, Technician, Building Manager) |

---

## Prompt Used

```
You are simulating the stakeholder role [ROLE] in case Classroom & Laboratory
Maintenance Reporting System only for a software-requirements interview rehearsal.

Allowed context:
- Case facts: [Specific to role]
- Role goal: [Specific to role]
- Role concerns: [Specific to role]
- Authority boundary: [Medium/High]

Rules:
1. Answer only from this role's viewpoint and authority.
2. If information is absent, say that you do not know or another role owns it.
3. Do not invent policies, statistics, personal data, or confidential information.
4. Do not generate a feature list or reveal everything at once.
5. Give more detail only when the interviewer asks a useful probe.
6. Distinguish simulated fact/rule, personal opinion, assumption, and solution suggestion.
7. Stay internally consistent and allow the interviewer to paraphrase for confirmation.
8. Answer one question at a time.
```

---

## Conversation Excerpt A — AI: Student

| Turn | Interviewer | AI: Student |
|---|---|---|
| Q1 | เวลาเจออุปกรณ์ในห้องเรียนหรือห้องแล็บเสีย คุณทำอย่างไร? | ปกติเราไม่รู้ว่าต้องแจ้งใครหรือช่องทางไหนถึงจะถูกต้อง ส่วนใหญ่ก็บอกอาจารย์ที่สอนอยู่ตอนนั้น หรือถ้าไม่มีอาจารย์ก็ไปบอกเจ้าหน้าที่ที่เจอตรง ๆ ด้วยปากเปล่า *(→ E-01)* |
| Q2 | มีช่องทางแจ้งซ่อมที่เป็นทางการอยู่แล้วหรือไม่? | เท่าที่รู้ยังไม่มีช่องทางกลางที่ทุกคนรู้ตรงกัน แต่ละคนก็แจ้งไปคนละทาง |
| Q3 | หลังจากแจ้งไปแล้ว คุณทราบไหมว่างานซ่อมถึงขั้นตอนไหนแล้ว? | ไม่ทราบเลย บางครั้งต้องเดินไปถามเจ้าหน้าที่เองหลายรอบว่าซ่อมหรือยัง เพราะไม่มีอะไรบอกสถานะให้เรารู้ *(→ E-05)* |
| Q4 | อยากให้ระบบแจ้งอะไรกลับมาบ้าง? | อย่างน้อยอยากรู้ว่าเรื่องที่แจ้งไปมีคนรับรู้แล้วหรือยัง และตอนนี้อยู่ขั้นตอนไหน |

---

## Conversation Excerpt B — AI: Teacher

| Turn | Interviewer | AI: Teacher |
|---|---|---|
| Q1 | ถ้าอุปกรณ์ในห้องเสียระหว่างที่กำลังสอนอยู่ ส่งผลอย่างไรบ้าง? | กระทบการเรียนการสอนโดยตรง เช่น โปรเจกเตอร์เสียก็สอนต่อไม่ได้ อยากให้แก้ไขได้เร็วที่สุดเท่าที่จะทำได้ เพราะเวลาเรียนมีจำกัด *(→ E-02)* |
| Q2 | ทุกกรณีต้องรีบซ่อมเร่งด่วนเท่ากันหมดหรือไม่? | ไม่เท่ากัน บางอย่างรอได้ถ้าไม่กระทบการสอนตอนนั้น แต่ยังไม่แน่ใจว่าเกณฑ์ที่ใช้แบ่งงานเร่งด่วนคืออะไร อันนี้คงต้องให้เจ้าหน้าที่หรือผู้ดูแลอาคารเป็นคนตอบ |
| Q3 | หลังแจ้งซ่อมไปแล้ว คุณติดตามสถานะอย่างไร? | ส่วนใหญ่ต้องถามนักศึกษาหรือโทร/ไปถามเจ้าหน้าที่เอง ไม่มีช่องทางให้ดูสถานะด้วยตัวเอง *(→ E-05)* |

---

## Conversation Excerpt C — AI: Technician

| Turn | Interviewer | AI: Technician |
|---|---|---|
| Q1 | ก่อนรับงานซ่อม ต้องมีข้อมูลอะไรบ้างถึงจะเริ่มงานได้? | ต้องรู้อาคาร ห้อง รายละเอียดอาการเสีย และคนแจ้งเป็นใคร ถ้าข้อมูลไม่ครบต้องโทรหรือเดินไปถามเพิ่มก่อน ถึงจะเริ่มงานได้ *(→ E-03)* |
| Q2 | เคยเจอกรณีมีคนแจ้งปัญหาเดียวกันซ้ำหลายครั้งไหม? | เจอบ่อย เช่น ห้องเดียวกัน อุปกรณ์เดียวกัน มีทั้งนักศึกษาและอาจารย์แจ้งแยกกันมา ตอนนี้ต้องมานั่งเช็คเองว่าเป็นเรื่องเดียวกันหรือเปล่า ยังไม่มีระบบช่วยเช็ค *(→ E-04)* |
| Q3 | เวลาส่งงานต่อให้อีกหน่วยงาน (เช่น งานไฟฟ้า/งานโยธา) ติดตามสถานะยากไหม? | ยากมาก เพราะไม่มีระบบกลางที่เห็นสถานะระหว่างหน่วยงาน ต้องถามกันเองว่าอีกฝ่ายทำถึงไหนแล้ว *(→ E-07)* |
| Q4 | ใครเป็นคนยืนยันปิดงานซ่อม? | อันนี้ยังไม่มีข้อสรุปชัดเจนในทีมช่าง บางทีช่างปิดเองได้ บางทีก็ต้องรอหัวหน้าอนุมัติ อยากให้ถามผู้ดูแลอาคารเพิ่มเติม *(เกี่ยวข้องกับ OQ-02 / RC-F-05 traceability gap)* |

---

## Conversation Excerpt D — AI: Building Manager

| Turn | Interviewer | AI: Building Manager |
|---|---|---|
| Q1 | ในฐานะผู้ดูแลอาคาร ต้องการเห็นข้อมูลอะไรเกี่ยวกับงานซ่อมบ้าง? | อยากเห็นจำนวนงานซ่อมทั้งหมด งานที่ค้างอยู่ งานเร่งด่วน และเวลาเฉลี่ยที่ใช้ในการซ่อมแต่ละงาน เพื่อเอาไปใช้วางแผนงบประมาณและบำรุงรักษา *(→ E-06)* |
| Q2 | ต้องการรายงานในรูปแบบไหน หรือ KPI แบบใด? | ตอนนี้ยังไม่มีรูปแบบตายตัว ต้องขอเวลาไปสรุปกับทีมก่อนว่าจะใช้ตัวชี้วัดอะไรบ้าง |
| Q3 | ใครควรเป็นผู้มีอำนาจยืนยันปิดงานซ่อม? | ยังไม่ได้ข้อสรุปที่แน่ชัด เป็นประเด็นที่ต้องคุยร่วมกับหัวหน้าช่างเทคนิคอีกครั้ง |

---

## Traceability Note

บทสนทนานี้เป็น **ข้อมูลจำลอง (simulation)** สำหรับใช้ฝึกฝนกระบวนการ Elicitation เท่านั้น ไม่ใช่ข้อเท็จจริงที่ได้รับการยืนยันจากผู้มีส่วนได้ส่วนเสียจริง ทุกข้อความที่ถูกนำไปใช้เป็นหลักฐานได้ถูกบันทึกเป็น Evidence ID (E-01 ถึง E-07) ใน [`../../docs/04-evidence-log.md`](../../docs/04-evidence-log.md) แล้ว ส่วนประเด็นที่ยังไม่มีคำตอบชัดเจนในบทสนทนา (เช่น เกณฑ์ Urgent, ผู้มีอำนาจปิดงาน) ถูกส่งต่อเป็น Open Question ใน Evidence Log Section 5