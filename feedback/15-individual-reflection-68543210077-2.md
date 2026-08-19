# 15 — Individual Reflection

## Student Information

| Field | Detail |
|---|---|
| Student ID | 68543210077-2 |
| Name | นายสันติ ปัญญาหน้อย |
| Primary Role(s) | Stakeholder Analysis / Requirements Analyst / Documentation |

---

## 1. My Contribution

ในโครงงาน Classroom & Laboratory Maintenance Reporting System (CLMRS) ข้าพเจ้ามีส่วนร่วมในการวิเคราะห์และจัดทำเอกสาร Requirements ตั้งแต่ Week 01 ถึง Week 08

งานที่รับผิดชอบหลัก ได้แก่

- จัดทำและปรับปรุง Problem Brief เพื่อสรุปปัญหาของระบบแจ้งซ่อม
- วิเคราะห์ Stakeholder และ User Needs ของนักศึกษา อาจารย์ เจ้าหน้าที่เทคนิค และผู้ดูแลอาคาร
- จัดทำ Evidence Log จากข้อมูลที่ได้จากการวิเคราะห์และสัมภาษณ์
- เปลี่ยน Evidence ให้เป็น Need และ Requirement Candidate
- จัดทำ Requirement Backlog และกำหนดประเภท Functional / NFR
- จัดลำดับ Requirement ด้วยแนวคิด MoSCoW
- ตรวจสอบ Traceability ระหว่าง Evidence → Need → Requirement
- วิเคราะห์ Open Questions และ Conflict / Unknown โดยเฉพาะกรณีการแจ้งปัญหาซ้ำ
- ช่วยตรวจสอบ Requirement ที่ยังไม่มีหลักฐานเพียงพอ และแยกออกจาก Final Requirement
- จัดทำ Validation และ Traceability ใน Week 08

ตัวอย่าง Requirement ที่ข้าพเจ้ามีส่วนวิเคราะห์ ได้แก่ Requirement เกี่ยวกับการแจ้งปัญหา การกรอกข้อมูลที่จำเป็น การจัดลำดับงาน Urgent การติดตามสถานะ การจัดการปัญหาที่แจ้งซ้ำ และการส่งต่องานระหว่างหน่วยงาน

---

## 2. What I Learned About Requirements and Design

ข้าพเจ้าได้เรียนรู้ว่า Requirement ไม่ควรถูกสร้างจากความคิดเห็นหรือความรู้สึกของทีมเพียงอย่างเดียว แต่ควรมี Evidence รองรับและสามารถตรวจสอบย้อนกลับได้

กระบวนการที่เข้าใจมากขึ้นคือ

Evidence → Need → Requirement Candidate → Requirement Backlog → Validation → Design

สิ่งที่ได้เรียนรู้ที่สำคัญคือ หากยังไม่มีข้อมูลเพียงพอ ไม่ควรรีบกำหนดเป็น Final Requirement แต่ควรบันทึกเป็น Open Question, Conflict หรือ Unknown เพื่อรอการตรวจสอบเพิ่มเติม

ตัวอย่างที่เห็นได้ชัดคือกรณี "การแจ้งปัญหาซ้ำ" ซึ่งทีมยังไม่สามารถสรุปได้ทันทีว่าระบบควรรวมรายการแจ้งซ้ำ เชื่อมกับรายการเดิม หรือปิดรายการใหม่ ดังนั้นจึงควรเก็บไว้เป็นประเด็นที่ต้องถาม Stakeholder ก่อน

นอกจากนี้ยังเข้าใจมากขึ้นว่า Requirement ที่ดีควรมี ID, Source, Rationale, Priority และสามารถนำไปตรวจสอบหรือสร้าง Test Case ได้

---

## 3. A Decision I Influenced

ข้าพเจ้ามีส่วนในการตัดสินใจให้ Requirement เกี่ยวกับ "การจัดการปัญหาที่แจ้งซ้ำ" ไม่ถูกกำหนดเป็นรายละเอียดของระบบแบบตายตัวทันที

จาก Evidence และ Need ที่เกี่ยวข้อง ทีมพบว่าปัญหาเดียวกันอาจถูกแจ้งจากหลายคน แต่ยังไม่มีข้อมูลยืนยันว่าหลังพบรายการซ้ำควรดำเนินการอย่างไร

จึงเสนอให้บันทึกประเด็นดังกล่าวเป็น Requirement Candidate / Needs Follow-up และ Open Question ก่อน โดยต้องสอบถามเจ้าหน้าที่เพิ่มเติมว่า

- ควรรวมรายการแจ้งซ้ำหรือไม่
- ควรเชื่อมรายการใหม่กับรายการเดิมหรือไม่
- ใครเป็นผู้ตัดสินใจว่าเป็นรายการซ้ำ
- รายการใดควรเป็นรายการหลัก

การตัดสินใจนี้ช่วยให้ทีมไม่สร้าง Business Rule ขึ้นมาเองโดยไม่มี Evidence รองรับ

---

## 4. Feedback I Received and How I Responded

จากการตรวจสอบเอกสารและ Traceability พบว่าบาง Requirement ยังเชื่อมโยงกับ Evidence และ Need ได้ไม่ชัดเจน รวมถึงบาง Requirement ยังมี Open Question ที่ต้องได้รับการยืนยันจาก Stakeholder

ข้าพเจ้าจึงปรับเอกสารโดย

- เพิ่ม Evidence / Need Trace ให้กับ Requirement
- แยก Requirement ที่มีหลักฐานชัดเจนออกจาก Requirement ที่ยังต้องตรวจสอบ
- เพิ่ม Open Question สำหรับประเด็นที่ยังไม่มีข้อมูลยืนยัน
- ปรับสถานะ Requirement เป็น `Ready for Week06` หรือ `Needs Follow-up` ตามระดับความพร้อม
- ตรวจสอบความสอดคล้องระหว่าง Requirement Candidate และ Requirement Backlog

นอกจากนี้ยังปรับไม่ให้ "LINE Notification" ถูกกำหนดเป็น Requirement โดยตรง เนื่องจากยังไม่มีหลักฐานยืนยันว่าช่องทางดังกล่าวเป็นความต้องการที่ได้รับการยืนยันจาก Stakeholder

---

## 5. What I Would Improve Next Time

หากทำงานลักษณะนี้อีกครั้ง ข้าพเจ้าจะวางโครงสร้าง Traceability ตั้งแต่เริ่มต้น โดยกำหนดความสัมพันธ์ระหว่าง Evidence, Need, Requirement และ Stakeholder ให้ชัดเจนตั้งแต่ Week แรก

สิ่งที่ต้องปรับปรุง ได้แก่

1. เก็บ Evidence ให้มีรายละเอียดมากขึ้นตั้งแต่ต้น
2. ระบุ Source และ Related Question ของแต่ละ Evidence ให้ชัดเจน
3. ตรวจสอบ Requirement ID และ Traceability ก่อนรวมเอกสาร
4. แยก Fact, Assumption และ Open Question ให้ชัดเจน
5. ไม่รีบกำหนดรายละเอียดของ Solution หากยังไม่มี Evidence
6. วางแผน Validation กับ Stakeholder ให้เร็วขึ้น
7. กำหนด Acceptance Criteria ควบคู่กับ Requirement ที่พร้อมพัฒนา
8. ตรวจสอบความสอดคล้องระหว่าง Requirement Backlog กับเอกสาร SRS ก่อนทำ Design

สิ่งสำคัญที่สุดที่ข้าพเจ้าจะนำไปใช้ในงานครั้งต่อไปคือ "ถ้ายังไม่มีหลักฐานเพียงพอ ไม่ควรเดา Requirement แต่ควรบันทึกสิ่งที่ยังไม่รู้และวางแผนตรวจสอบต่อ"

---

## 6. Evidence Links

- `docs/01-problem-brief.md`
- `docs/02-stakeholder-context-scope.md`
- `docs/04-evidence-log.md`
- `docs/04-requirement-candidates.md`
- `docs/05-requirement-backlog.md`
- `docs/05-open-questions-and-issues.md`
- `docs/05-prioritization-rationale.md`
- `docs/08-validation-traceability.md`
- Git commit history ของการปรับปรุง Requirements และ Traceability
