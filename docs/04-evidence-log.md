# Initial Requirement Candidates — Classroom & Laboratory Maintenance Reporting System

> **Status:** Initial candidates from Week 03 planning and interview preparation.  
> **สถานะ:** Candidate Requirements เบื้องต้นจากการวางแผนและการเตรียมสัมภาษณ์ใน Week 03  
> **These are not yet approved requirements or an SRS.**  
> **ยังไม่ใช่ Requirement ที่ได้รับการยืนยันหรือเอกสาร SRS**  
> **Week 04 will collect evidence from stakeholders, and Week 05 will analyze, categorize, and refine these requirements.**  
> **Week 04 จะเก็บหลักฐาน (Evidence) จากผู้มีส่วนได้ส่วนเสีย และ Week 05 จะนำมาวิเคราะห์ จัดหมวดหมู่ และปรับปรุง Requirement ให้สามารถตรวจสอบได้**

| ID | Candidate Type | Initial Candidate | Source / Planned Evidence | Confidence | Open Validation |
|---|---|---|---|---|---|
| RC-F-01 | Functional | ระบบควรให้ผู้ใช้งานสามารถแจ้งปัญหาอุปกรณ์หรือห้องเรียนที่ชำรุดได้ | Student / Teacher Interview | Medium | ต้องยืนยันข้อมูลที่จำเป็นในการแจ้งซ่อม |
| RC-F-02 | Functional | ระบบควรบันทึกข้อมูลที่จำเป็นต่อการดำเนินงานของเจ้าหน้าที่ เช่น สถานที่ รายละเอียดปัญหา และหลักฐานประกอบ | Technician Interview | Medium | ต้องยืนยันรายการข้อมูลที่จำเป็นทั้งหมด |
| RC-F-03 | Functional | ระบบควรสนับสนุนการจัดลำดับความสำคัญของงานซ่อมตามระดับความเร่งด่วน | Technician + Manager Interview | Low | ต้องยืนยันเกณฑ์ Priority |
| RC-F-04 | Functional | ระบบควรให้เจ้าหน้าที่สามารถติดตามสถานะงานและบันทึกผลการดำเนินงานได้ | Technician Workflow | Medium | ต้องยืนยัน Workflow และขั้นตอนการปิดงาน |
| RC-F-05 | Functional | ระบบควรให้ผู้ใช้งานสามารถติดตามความคืบหน้าของรายการแจ้งซ่อมของตนเองได้ | Student / Teacher Interview | Low | ต้องยืนยันข้อมูลที่ต้องการและวิธีการติดตาม |
| RC-F-06 | Functional | ระบบควรรองรับการจัดการกรณีแจ้งปัญหาซ้ำและการส่งต่องานระหว่างหน่วยงาน | Technician + Manager Interview | Low | ต้องยืนยันขั้นตอนการจัดการงานซ้ำและการส่งต่องาน |
| RC-F-07 | Functional | ระบบควรสนับสนุนการยืนยันการซ่อมเสร็จสิ้นโดยผู้รับผิดชอบที่กำหนด | Technician + Manager Interview | Low | ต้องยืนยันผู้มีอำนาจในการปิดงาน |
| RC-F-08 | Functional | ผู้ดูแลอาคารหรือผู้บริหารควรสามารถดูรายงานสรุปงานซ่อมเพื่อใช้ติดตามและวางแผนการบำรุงรักษาได้ | Manager Interview | Medium | ต้องยืนยันข้อมูลและตัวชี้วัดที่ต้องการ |

| RC-NF-01 | Non-functional | ระบบควรใช้บัญชีของมหาวิทยาลัยในการยืนยันตัวตนและกำหนดสิทธิ์การใช้งานตามบทบาท | IT / University Policy | Medium | ต้องยืนยัน Role Mapping |
| RC-NF-02 | Non-functional | ผู้ใช้งานแต่ละบทบาทควรเห็นข้อมูลตามสิทธิ์ที่ได้รับ | Privacy Analysis + IT | Medium | ต้องยืนยัน Access Control Matrix |
| RC-NF-03 | Non-functional | ระบบควรแสดงสถานะงานซ่อมที่เป็นปัจจุบันและสามารถตรวจสอบย้อนหลังได้ | Student + Technician Interview | Low | ต้องยืนยันความถี่ในการอัปเดตสถานะ |
