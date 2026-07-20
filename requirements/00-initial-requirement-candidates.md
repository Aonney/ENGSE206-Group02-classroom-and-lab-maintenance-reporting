
# Initial Requirement Candidates — Classroom & Laboratory Maintenance Reporting System

> **สถานะ:** ข้อกำหนดเบื้องต้น (Initial Requirement Candidates) ที่ได้จากการวางแผนและการซ้อมสัมภาษณ์ใน **Week 03**  
> **เอกสารนี้ยังไม่ใช่ Software Requirements Specification (SRS) และยังไม่ใช่ Requirement ที่ได้รับการยืนยันหรืออนุมัติแล้ว**  
> ใน **Week 04** ทีมจะเก็บหลักฐาน (Evidence) จากการสัมภาษณ์และการเก็บข้อมูลจาก Stakeholders และใน **Week 05** จะนำข้อมูลมาวิเคราะห์ จัดหมวดหมู่ และปรับข้อความของ Requirements ให้มีความชัดเจน สามารถตรวจสอบและยืนยันได้

| ID | Candidate Type | Initial Candidate | Source / Planned Evidence | Confidence | Open Validation |
|---|---|---|---|---|---|
| RC-F-01 | Functional | ระบบควรให้ผู้ใช้งานแจ้งปัญหาอุปกรณ์หรือห้องเรียน พร้อมระบุรายละเอียด ตำแหน่ง และแนบรูปภาพได้ | Student + Teacher interview | Medium | ข้อมูลใดจำเป็นต่อการแจ้งซ่อมจริง |
| RC-F-02 | Functional | ระบบควรให้ผู้แจ้งสามารถติดตามสถานะของรายการแจ้งซ่อมได้ | Student interview | Medium | ผู้ใช้ต้องการเห็นสถานะใดบ้าง |
| RC-F-03 | Functional | ระบบควรช่วยลดการแจ้งปัญหาซ้ำ โดยตรวจสอบหรือแสดงรายการแจ้งที่มีอยู่แล้ว | Student + Technician interview | Low | วิธีตรวจสอบงานซ้ำควรเป็นอย่างไร |
| RC-F-04 | Functional | เจ้าหน้าที่เทคนิคควรได้รับรายการแจ้งซ่อมใหม่ และสามารถอัปเดตสถานะการดำเนินงานได้ | Technician workflow | High | รายละเอียดของแต่ละสถานะมีอะไรบ้าง |
| RC-F-05 | Functional | ระบบควรรองรับการกำหนดลำดับความสำคัญของงานซ่อมตามประเภทของปัญหา | Technician + Manager interview | Medium | เกณฑ์การกำหนดงานเร่งด่วนคืออะไร |
| RC-F-06 | Functional | ระบบควรบันทึกผลการซ่อม วันที่ดำเนินการ และผู้รับผิดชอบเมื่อปิดงาน | Technician interview | Medium | ใครเป็นผู้ยืนยันการปิดงาน |
| RC-F-07 | Functional | ระบบควรแจ้งเตือนผู้แจ้งเมื่อสถานะของงานซ่อมมีการเปลี่ยนแปลง | Student + Teacher interview | Low | ช่องทางและช่วงเวลาการแจ้งเตือนที่เหมาะสม |
| RC-F-08 | Functional | ผู้ดูแลอาคารหรือผู้บริหารควรสามารถดูรายงานและสถิติงานซ่อมเพื่อใช้วางแผนการบำรุงรักษาได้ | Manager interview | Medium | ต้องการ KPI หรือรายงานประเภทใด |

| RC-NF-01 | Non-functional | ระบบควรใช้บัญชีมหาวิทยาลัยในการยืนยันตัวตนและกำหนดสิทธิ์การเข้าถึงตามบทบาท | Privacy analysis + stakeholder interview | Medium | Role และสิทธิ์ของแต่ละผู้ใช้ |
| RC-NF-02 | Non-functional | ผู้ใช้แต่ละบทบาทควรเข้าถึงเฉพาะข้อมูลที่เกี่ยวข้องกับหน้าที่ของตน | Privacy & Access Control | Medium | Access Matrix ยังต้องยืนยัน |
| RC-NF-03 | Non-functional | ระบบควรปกป้องข้อมูลส่วนบุคคลและเก็บเฉพาะข้อมูลที่จำเป็นต่อการแจ้งซ่อม | Privacy discussion | High | ต้องตรวจสอบรายการข้อมูลที่จำเป็น |
| RC-NF-04 | Non-functional | ระบบควรแสดงข้อมูลสถานะงานที่เป็นปัจจุบัน เพื่อลดความสับสนของผู้ใช้งาน | Student pain points | Medium | ความถี่ในการอัปเดตข้อมูลควรเป็นเท่าใด |

---

## Rule for Week 04–05

เมื่อได้หลักฐาน (Evidence) จากการสัมภาษณ์หรือการสังเกต ให้เพิ่ม **Evidence ID** และปรับระดับ **Confidence (Low / Medium / High)** พร้อมบันทึกเหตุผลประกอบ หากพบข้อมูลที่ขัดแย้งกันจาก Stakeholder หลายกลุ่ม ให้บันทึกเป็นประเด็น (Issue) และตรวจสอบเพิ่มเติมก่อนสรุปเป็น Requirement ของระบบ
