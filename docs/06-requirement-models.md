# 06 — Requirement Models: User Stories, Use Cases and Acceptance Criteria

> **Week 6 deliverable**

## 1. User Stories

| ID | User Story | Priority | Linked FR | Acceptance Criteria |
|---|---|---|---|---|
| US-01 | As a [role], I want [goal] so that [benefit]. | Must | FR-01 | AC-01, AC-02 |

## 2. Acceptance Criteria

### AC-01 — [ชื่อ]

- Given [initial context]
- When [action]
- Then [expected result]

## 3. Use Case List

| ID | Use Case | Primary Actor | Goal | Related FR | Diagram |
|---|---|---|---|---|---|
| UC-01 | แจ้งปัญหาอุปกรณ์ / ห้องเรียน | นักศึกษา / ผู้ใช้งานห้อง | แจ้งปัญหาและได้รับเลขที่อ้างอิง | FR-CLMRS-01, FR-CLMRS-02 | `../diagrams/use-case/UC-01-report-issue.md` |
| UC-02 | ติดตามสถานะงานซ่อม | นักศึกษา / ผู้ใช้งานห้อง | ตรวจสอบสถานะงานของตนเอง | FR-CLMRS-04 | `../diagrams/use-case/UC-02-track-issue.md` |
| UC-03 | จัดลำดับงานซ่อม | เจ้าหน้าที่เทคนิค | จัดลำดับงานตามความเร่งด่วน | FR-CLMRS-03 | `../diagrams/use-case/UC-03-prioritize-issue.md` |
| UC-04 | ตรวจสอบรายการแจ้งซ้ำ | เจ้าหน้าที่เทคนิค | ตรวจสอบและจัดการรายการซ้ำ | FR-CLMRS-05 | `../diagrams/use-case/UC-04-duplicate-issue.md` |
| UC-05 | บันทึกผลและปิดงานซ่อม | เจ้าหน้าที่เทคนิค | บันทึกผลการซ่อมและปิดงาน | FR-CLMRS-06 | `../diagrams/use-case/UC-05-close-work.md` |
| UC-06 | ส่งต่อและติดตามงาน | เจ้าหน้าที่เทคนิค | ติดตามงานที่ส่งต่อระหว่างหน่วยงาน | FR-CLMRS-07 | `../diagrams/use-case/UC-06-forward-work.md` |
| UC-07 | แจ้งเตือนสถานะงาน | ระบบ / ผู้ใช้งาน | แจ้งผู้ใช้งานเมื่อสถานะเปลี่ยน | FR-CLMRS-08 | `../diagrams/use-case/UC-07-notification.md` |
| UC-08 | ดูรายงานงานซ่อม | ผู้ดูแลอาคาร / ผู้บริหาร | ดูภาพรวมและสถิติงานซ่อม | FR-CLMRS-09 | `../diagrams/use-case/UC-08-maintenance-report.md` |
| UC-09 | ควบคุมสิทธิ์การเข้าถึง | ระบบ | จำกัดการเข้าถึงตามบทบาท | NFR-CLMRS-01 | `../diagrams/use-case/UC-09-access-control.md` |

## 4. Use Case Specification

### UC-01 — [ชื่อ Use Case]

| Field | Detail |
|---|---|
| Primary Actor | [กรอก] |
| Trigger | [กรอก] |
| Preconditions | [กรอก] |
| Main Success Scenario | 1. ... 2. ... |
| Alternate / Exception Flows | [กรอก] |
| Postconditions | [กรอก] |
| Related Requirements | FR-xx, NFR-xx |

## 5. Requirement Models / Diagrams

- Use Case Diagram: [link](../diagrams/use-case/README.md)
- Activity Diagram: [link](../diagrams/activity/README.md)
- Domain Model: [link](../diagrams/domain-model/README.md)

## 6. Negotiation / Trade-off Notes

บันทึกสิ่งที่ไม่ได้เลือกหรือเลื่อนออกจาก scope พร้อมเหตุผล

[กรอก]
