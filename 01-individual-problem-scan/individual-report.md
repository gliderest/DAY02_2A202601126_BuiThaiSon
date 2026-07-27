# 01 — Individual Problem Scan

## Scan rộng

Sơn scan 10 problems, vượt mức tối thiểu 5. 

| # | Lăng kính | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại | Mỗi thứ Hai tổng hợp Weekly Report từ Jira, Sheets, Slack | PM, EM, CEO | Mất khoảng 90 phút/tuần |
| 2 | Lặp lại | Copy sprint velocity từ Jira vào slide update | PM | Lặp lại mỗi tuần |
| 3 | Tốn thời gian | Review PRD 10-15 trang trước khi comment | PM reviewer, design lead | 45 phút/bản |
| 4 | Tốn thời gian | Viết meeting notes sau cross-team meeting | PM, team member | 30 phút/buổi |
| 5 | AI có thể tốt hơn | Notion không gợi ý priority theo deadline/context | PM, team member | Task nhiều nhưng priority mơ hồ |
| 6 | AI có thể tốt hơn | Slack search tìm decision cũ rất khó | Cả team | 10-15 phút/lần tìm |
| 7 | Pain từ người khác | Designer phải hỏi lại vì spec từ PM mập mờ | Designer, PM | Hỏi lại 2-3 lần/spec |
| 8 | Pain từ người khác | CEO hỏi update nhưng report chưa sẵn | CEO, PM | Hay bị trễ deadline thứ Hai |
| 9 | Tốn thời gian | Tổng hợp monthly KPI từ nhiều dashboard | PM, manager | Lặp lại mỗi tháng |
| 10 | Lặp lại | Viết standup update mỗi sáng cùng format | PM | 5-10 phút/ngày |

Vì sao phần scan này mạnh:

- Có scan rộng trước khi hội tụ.
- Có nhiều lăng kính khác nhau.
- Mỗi problem có actor và dấu hiệu thật.
- Không bắt đầu bằng "làm chatbot" hoặc "xây agent".

## Top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Weekly Report | Workflow rõ, mất nhiều thời gian, có metric tốt | Narrative "đủ tốt" đo thế nào |
| 2 | Review PRD | Có pain thật, AI có thể giúp đọc/tóm tắt | Quality improvement khó đo |
| 3 | Slack Search | Nhiều người đau, impact rộng | Data access khó, scope có thể quá lớn |

## Problem Card #1 — Weekly Report

**Problem 1 câu:**  
Mỗi thứ Hai PM mất khoảng 90 phút tổng hợp Weekly Report từ nhiều nguồn, trong đó bước viết narrative tốn nhất và dễ trễ deadline.

**Actor:**  
Junior PM chịu trách nhiệm gửi weekly report cho Engineering Manager và CEO.

**Thời điểm / bối cảnh:**  
Thứ Hai hằng tuần, trước buổi leadership sync.

**Current workflow:**

```text
1. Export Jira sprint data
2. Lấy metrics từ Google Sheets
3. Đọc Slack recap tuần
4. Tổng hợp vào Google Docs
5. Viết narrative: insight, highlight, risk, next action
6. Self-review + format
7. Gửi email cho stakeholders
```

**Bottleneck:**  
Bước 5 — viết narrative từ raw data mất khoảng 25 phút và hay bị blank page.

**Impact:**  
90 phút/tuần cho 1 PM. Team có 3 PM nên tổng công sức có thể khoảng 270 phút/tuần. Báo cáo trễ làm leadership thiếu bối cảnh trước buổi sync.

**Success metric:**  
Giảm tổng thời gian từ 90 phút xuống dưới 30 phút, không tăng số câu CEO/EM phải hỏi lại.

**Non-AI alternative:**  
Template report + Jira dashboard + checklist có thể giảm format effort, nhưng chưa giải quyết tốt phần viết narrative.

**AI hypothesis:**  
AI hỗ trợ cấu trúc dữ liệu và draft narrative. PM vẫn review/edit trước khi gửi.

**Quick gut:**  
Workflow.

### Draft current workflow

```text
CURRENT STATE — 90 phút

[1 Export Jira: 10']
→ [2 Lấy metrics: 10']
→ [3 Đọc Slack: 15']
→ [4 Tổng hợp vào Docs: 15']
→ [5 Viết narrative: 25']  <-- bottleneck
→ [6 Review + format: 10']
→ [7 Gửi: 5']
```

### Draft future workflow

```text
FUTURE STATE — 21 phút

[1 Auto-pull data: 2']
→ [2 AI cấu trúc dữ liệu: 1']
→ [3 AI draft narrative: 1']
→ [4 PM review + edit: 15']  <-- human boundary
→ [5 PM gửi: 2']

Fallback: AI draft tệ → PM tự viết lại.
```

## Problem Cards #2 và #3 — tóm tắt

| Card | Actor | Bottleneck | Metric | Quick gut | Vì sao chưa chọn làm #1 |
|---|---|---|---|---|---|
| Review PRD | PM reviewer | Đọc 10-15 trang để hiểu context | 45 phút → 20 phút | Workflow | Quality metric khó hơn |
| Slack Search | Team member | Search keyword rồi đọc thread | 15 phút → dưới 2 phút | Agent / Workflow | Data access và scope rộng |