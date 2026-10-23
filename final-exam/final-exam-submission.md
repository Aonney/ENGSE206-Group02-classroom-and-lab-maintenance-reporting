# ใบส่งงานสอบปลายภาค — ส่วน ก งานกลุ่ม (Change-to-Design)

> วางไฟล์นี้ที่ `final-exam/final-exam-submission.md` ใน branch `final-exam` ของ Team Repo · ถ้อยคำในวงเล็บเป็นคำแนะนำ ลบได้

| รายการ | กรอก |
|---|---|
| กลุ่ม / Case | กลุ่ม 02 · Case 02 |
| ชื่อระบบ | ระบบแจ้งซ่อมอุปกรณ์ในห้องเรียนและห้องปฏิบัติการ (CLMRS) |
| CR เสริมที่เลือก | CR-FX-02A ใช้งานหน้างาน: สแกน QR + สัญญาณไม่เสถียร |
| Branch | `final-exam` |
| Pull Request | `submit(final): change-to-design take-home` |
| Commit hash สุดท้าย (ก่อน T0 + 24 ชั่วโมง) | `0c16c99` (commit สุดท้ายของเนื้อหางาน · commit ถัดไปแก้เฉพาะบรรทัดนี้) |
| สถานะ SRS ที่ใช้เป็นฐาน | Baseline Candidate (SRS v2.1) |

## งานเดิมที่ใช้เป็นฐาน

| งาน | ไฟล์และ commit หรือวันที่ |
|---|---|
| SRS (W07) | `docs/07-srs-v2.md` v2.1 · commit `5b2cf79` (22/09/2026) |
| งาน W08 (review · trace · CR) | `docs/08-validation-traceability.md` · commit `a2248e5` (19/08/2026) |
| Design Strategy + Design Spine (W10) | ไม่มีงานเดิม (`design/10-design-strategy.md` · `design/00-design-spine.md` ยังเป็น template) — G3 เริ่มจาก SRS v2.1 |
| Conceptual Architecture (W11) | ไม่มีงานเดิม (`diagrams/architecture/` ว่าง) — G4 วาด Context/Container ใหม่ทั้งภาพ |

## ไฟล์ที่ส่ง

- [x] `final-exam/final-exam-group-answer.docx`
- [x] `final-exam/diagrams/context-after.drawio` + `.png`
- [x] `final-exam/diagrams/container-after.drawio` + `.png`
- [x] `final-exam/final-exam-submission.md` (ไฟล์นี้)
- [x] `final-exam/ai-use-log.md`

## สมาชิกและส่วนที่รับผิดชอบ

| ชื่อ–สกุล | รหัส | รับผิดชอบ (G / ข้อ) | หลักฐาน (commit หรือส่วนในไฟล์) |
|---|---|---|---|
| นายสันติ ปัญญาหน้อย | 68543210077-2 | G2 · G3 | `95a6a6dd` G2 แก้ Requirement และ Model, G3 Design |
| นายธีรนัย ไชยกันทะ | 68543210066-5 | G1 · G5 · G6 · รวมไฟล์ Word · ใบส่งงาน · PR | `7341e01` หัวแบบฟอร์ม · `1bb0227` G1 · `ebb35ca` AI log · `b3bc263` `4d99719` แก้ G2–G3 · `a94302e` G5 · `d1ecbd7` G6 |
| นายบูรพา ประทีปรัตน์ | 68543210032-7 | G4 (Context · Container · ตาราง 4.3–4.6) | `35022aa2` G4 V1 . `c2354006` G4 finish . `cdae4c27` Update Ai log |

## รับรอง

- [x] สมาชิกทุกคนอ่านคำตอบทั้งฉบับ และอธิบายส่วนใดก็ได้ใน oral spot-check
- [x] ไม่มีตัวเลข นโยบาย หรือ protocol ที่แต่งขึ้น — ค่าที่ไม่รู้เป็น TBD และมี OI หรือ DD รองรับ
- [x] ไม่อ้างว่า SRS หรือ CR ใด Approved
- [x] ไม่ได้แก้ไฟล์งานเดิมของแต่ละสัปดาห์ — ทุกอย่างอยู่ใน `final-exam/`
