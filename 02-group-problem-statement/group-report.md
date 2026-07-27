# 02 — Group Problem Statement


## Thành viên nhóm


| STT | Họ và tên        | Mã học viên | Vai trò trong nhóm      | Phân công cụ thể                                                                |
| --- | ---------------- | ----------- | ----------------------- | ------------------------------------------------------------------------------- |
| 1   | Bùi Thái Sơn     | 2A202601126 | Research                | Research giải pháp đã có (Zotero, Mendeley, Paperpile), tìm nguồn uy tín        |
| 2   | Nguyễn Văn Trọng | 2A202601102 | Workflow                | Vẽ workflow trước/sau, xác định bottleneck và AI intervention point             |
| 3   | Nguyễn Hùng Mạnh | 2A202601256 | Metric                  | Xây dựng baseline, success metric, before/after impact table                    |
| 4   | Đoàn Ngọc Linh   | 2A202601762 | Research                | Research thêm nguồn học thuật (Semantic Scholar API, CrossRef), kiểm chứng link |
| 5   | Nguyễn Tiến Đạt  | 2A202601850 | Pain point & Validation | Quick interview, mini poll, thu thập tín hiệu pain thật từ sinh viên            |


---


## Group convergence


Nhóm 5 người, mỗi người share top 3. Tổng cộng 15 candidates, sau đó chọn ra 4 candidates cuối cùng.


| Cluster                  | Candidates included                                                                               | Pattern chung                                                       |
| ------------------------ | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| A — Code & Debug         | Debug lỗi runtime/logic, viết boilerplate CRUD, viết unit test, nối lại mạch khi quay lại repo cũ | Lập trình viên gặp vấn đề lặp lại / tốn thời gian khi code          |
| B — Nội dung & Trình bày | Đăng nội dung lên nhiều kênh, chuyển paper thành slide, tổng hợp và viết lại từ nhiều tài liệu    | Chuyển thông tin thô thành sản phẩm có cấu trúc                     |
| C — Học tập & Ôn bài     | Tìm lại chi tiết sau buổi họp/học, tạo flashcard, đọc/lọc PDF tìm trích dẫn, gom bài tập nhóm     | Sinh viên mất thời gian tổng hợp thông tin rời rạc                  |
| D — Citation & Reference | Quản lý tham khảo và citation, kiểm tra citation/định dạng reference, literature review           | Kiểm tra, chuẩn hóa và chèn citation thủ công tốn thời gian, dễ sai |


Nhóm nhận thấy Cluster D có pain rõ nhất, actor cụ thể (sinh viên viết bài), workflow tuyến tính và metric dễ đo.


## Shortlist và score


| Candidate                                | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
| ---------------------------------------- | -------: | ----------: | ---------------: | -------------: | ------------: | -----------------: | ---------------: | ---: |
| Quản lý citation và reference            |        5 |           5 |                5 |              4 |             5 |                  5 |                5 |   34 |
| Tìm và thu thập paper từ nhiều nguồn     |        4 |           4 |                4 |              3 |             5 |                  4 |                4 |   28 |
| Tóm tắt literature review từ nhiều paper |        4 |           4 |                4 |              3 |             5 |                  4 |                4 |   28 |


Nhóm chọn: **Quản lý citation và reference**.


Vì sao chọn:


- Workflow rõ ràng: tìm tài liệu → thu thập metadata → chèn citation → kiểm tra reference list.
- Pain thật: sinh viên thường mất thời gian sửa citation và reference thủ công trước khi nộp.
- Validate được nhanh bằng Zotero, Mendeley, Word hoặc Overleaf.
- Nhiều tool/pattern có sẵn để research và so sánh.
- Vẽ before/after workflow rất rõ.


Vì sao không chọn các bài khác:


- Tìm và thu thập paper: impact rộng nhưng phân loại và chuẩn hóa nguồn phức tạp, scope quá lớn cho lab.
- Tóm tắt literature review: workflow rõ nhưng quality metric khó thống nhất trong thời gian lab.


---


## Quick validation


Nhóm hỏi nhanh 5 sinh viên và poll 8 người trong lớp.


| Nguồn               | Số người | Tín hiệu xác nhận                                                      | Tín hiệu phản bác                                       | Nhóm sửa problem thế nào                                                                             |
| ------------------- | -------: | ---------------------------------------------------------------------- | ------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| Quick interview     |        5 | 4/5 người từng phải sửa citation hoặc reference thủ công trước khi nộp | 1 người đã dùng Zotero nên pain giảm nhiều              | Thu hẹp problem: không phải "tự động tạo citation tổng quát", mà là "kiểm tra và chuẩn hóa citation" |
| Mini poll trong lớp |        8 | 6/8 từng gặp lỗi citation hoặc thiếu reference                         | Một số người dùng tool hỗ trợ nên chỉ cần kiểm tra thêm | Thêm non-AI alternative: Zotero/Mendeley + template citation                                         |


Insight sau validation:


```text
Pain thật không nằm ở việc "copy citation". Pain nằm ở việc kiểm tra tính đúng, nhất quán và sửa thủ công trước khi nộp.
```


---


## Research giải pháp


Nhóm tìm các hướng đã có sẵn, không giả định phải tự build từ đầu.


| Nguồn / tool / case                   | Link                                                            | Họ giải quyết phần nào?                            | Điểm mạnh                                                               | Khoảng trống / rủi ro                                               | Bài học cho nhóm                                                                   |
| ------------------------------------- | --------------------------------------------------------------- | -------------------------------------------------- | ----------------------------------------------------------------------- | ------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| Zotero (open-source)                  | https://www.zotero.org                                          | Quản lý reference, tạo citation, sync library      | Miễn phí, plugin Word/Google Docs, hỗ trợ 10.000+ citation styles (CSL) | Metadata import từ web có thể thiếu/sai, cần user kiểm tra thủ công | Dùng làm base workflow; AI nên hỗ trợ bước kiểm tra metadata mà Zotero chưa tự làm |
| Mendeley Reference Manager (Elsevier) | https://www.mendeley.com/reference-management/reference-manager | Chèn citation trong Word, quản lý PDF và reference | Tích hợp tốt với Word, auto-extract metadata từ PDF                     | Vẫn cần kiểm tra thủ công; bản miễn phí giới hạn storage            | Pattern tốt: tool làm phần import, người dùng vẫn phải review                      |
| CrossRef REST API                     | https://api.crossref.org/swagger-ui/index.html                  | Tra cứu metadata chính thức của paper qua DOI      | Nguồn metadata uy tín nhất (từ nhà xuất bản), API miễn phí              | Chỉ cover paper có DOI, không cover sách/web/thesis                 | AI có thể gọi CrossRef API để verify metadata thay vì đoán                         |
| Semantic Scholar API (Allen AI)       | https://api.semanticscholar.org/                                | Tìm paper, lấy metadata, citation graph            | API miễn phí, có abstract, author, citation count                       | Không phủ toàn bộ ngành, metadata đôi khi trễ                       | Dùng như nguồn bổ sung để cross-check metadata                                     |


Research takeaway:


```text
Không nên build agent tự làm toàn bộ citation. Hướng hợp lý: Workflow — thu thập reference bằng Zotero/Mendeley → AI gọi CrossRef/Semantic Scholar API kiểm tra metadata → AI gợi ý format citation → người dùng review trước khi nộp.
```


---


## Workflow before/after


```text
CURRENT STATE — 6 bước, 20–30 phút


[1 Thu thập paper/source: 5–10']
→ [2 Copy metadata thủ công: 5–10']       <-- bottleneck
→ [3 Chọn style citation: 3–5']
→ [4 Chèn citation vào văn bản: 5–10']    <-- bottleneck
→ [5 Kiểm tra reference list: 5–10']      <-- bottleneck chính
→ [6 Sửa lỗi thủ công: 5–10']


FUTURE STATE — 4 bước, 8–10 phút


[1 Import source vào Zotero/Mendeley: 2']           -- Rule/tool
→ [2 AI kiểm tra metadata qua CrossRef API: 2']     -- AI step
→ [3 AI gợi ý format chuẩn + kiểm tra consistency: 3']  -- AI step
→ [4 Người dùng review + xác nhận: 3–4']            <-- human boundary


Fallback: AI gợi ý sai hoặc thiếu metadata → người dùng sửa thủ công như trước.
Bottleneck mới: Review + xác nhận — chấp nhận được vì là bước kiểm soát chất lượng.
```


Before/after impact:


| Metric           |                    Trước |           Sau kỳ vọng | Ghi chú                          |
| ---------------- | -----------------------: | --------------------: | -------------------------------- |
| Tổng thời gian   |               20–30 phút |             8–10 phút | Target chính                     |
| Số bước          |                        6 |                     4 | Giảm thao tác thủ công           |
| Bước thủ công    |                      6/6 |                   1/4 | Người dùng chỉ review + xác nhận |
| Bottleneck chính | Kiểm tra và sửa citation |        Review/confirm | Human boundary                   |
| Risk mới         |         Không có AI risk | AI gợi ý sai metadata | Cần review trước khi nộp         |


---


## Problem Statement v0


| Field              | Nội dung                                                                                                            |
| ------------------ | ------------------------------------------------------------------------------------------------------------------- |
| **Actor**          | Sinh viên, nghiên cứu sinh chịu trách nhiệm hoàn thiện bài viết và reference list.                                  |
| **Workflow**       | Thu thập paper/source → copy metadata → chọn citation style → chèn citation → kiểm tra reference list → sửa lỗi.    |
| **Bottleneck**     | Kiểm tra và sửa citation thủ công mất nhiều thời gian và dễ sai, đặc biệt khi nguồn có nhiều định dạng khác nhau.   |
| **Impact**         | Một bài viết có thể mất 20–30 phút để hoàn thiện citation; sai citation làm chậm việc nộp bài hoặc giảm chất lượng. |
| **Success Metric** | Giảm thời gian từ 20–30 phút xuống 8–10 phút; giảm số lỗi citation xuống 0 lỗi format trước khi nộp.                |
| **Boundary**       | AI không tự nộp bài; không tự chỉnh sửa nội dung bài viết; chỉ gợi ý và kiểm tra citation.                          |


---


## Rule / Workflow / Agent


| Mức          | Phương án cho bài toán nhóm                                                           | Khi nào đủ                                                  | Rủi ro                                       | Chọn?                                              |
| ------------ | ------------------------------------------------------------------------------------- | ----------------------------------------------------------- | -------------------------------------------- | -------------------------------------------------- |
| **Rule**     | Template citation style, auto-import từ Zotero/Mendeley                               | Đủ nếu người dùng chỉ cần format chuẩn                      | Không kiểm tra được metadata sai/thiếu       | Không chọn làm toàn bộ, nhưng dùng cho bước import |
| **Workflow** | Import source → AI kiểm tra metadata (CrossRef API) → AI gợi ý citation → user review | Hợp vì workflow tuyến tính, AI hỗ trợ bước kiểm tra rõ ràng | AI gợi ý sai metadata khi paper không có DOI | Chọn                                               |
| **Agent**    | Agent tự thu thập, kiểm tra, cập nhật citation và reference list                      | Chỉ cần nếu workflow nhiều nhánh, tự quyết bước tiếp theo   | Quá rộng, dễ sai khi tự động hóa toàn bộ     | Chưa chọn                                          |


Mức chọn: **Workflow**


Vì sao:


- Thu thập dữ liệu có thể dùng rule/tool (Zotero/Mendeley).
- Kiểm tra metadata cần AI gọi API (CrossRef, Semantic Scholar) để verify.
- Người dùng vẫn review nên risk kiểm soát được.
- Chưa cần agent vì workflow không cần tự lập kế hoạch động.


Vì sao không chọn mức đơn giản hơn:


- Rule/template chỉ giải quyết format, không kiểm tra được metadata sai/thiếu/không nhất quán — đây mới là pain chính.


---


## Problem Statement v1


| Field                            | Nội dung                                                                                                                      |
| -------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **Actor**                        | Sinh viên, nghiên cứu sinh chịu trách nhiệm hoàn thiện bài viết học thuật.                                                    |
| **Workflow**                     | Thu thập source → kiểm tra metadata → chọn citation style → chèn citation → kiểm tra reference list → sửa lỗi.                |
| **Bottleneck**                   | Kiểm tra và sửa citation thủ công mất 20–30 phút và dễ sai khi nguồn có nhiều định dạng.                                      |
| **Impact**                       | 20–30 phút/bài viết; sai citation làm chậm nộp bài và giảm chất lượng học thuật.                                              |
| **Success Metric**               | Giảm thời gian xuống 8–10 phút; 0 lỗi format citation trước khi nộp.                                                          |
| **Boundary**                     | AI không tự nộp bài, không tự thay đổi nội dung, chỉ hỗ trợ kiểm tra và gợi ý citation.                                       |
| **AI intervention point**        | Sau khi source đã được import vào tool, trước khi hoàn thiện reference list và nộp.                                           |
| **Mức chọn**                     | Workflow: Zotero/Mendeley import + AI kiểm tra metadata (CrossRef API) + AI gợi ý citation + user review.                     |
| **Rủi ro & người thật kiểm tra** | Risk: metadata sai khi paper không có DOI, citation không đúng style. Người thật: user phải review và xác nhận trước khi nộp. |


---


## Final decision


Decision: **Go với scope nhỏ.**


Pilot nhỏ nhất:


- Dùng 2–3 tài liệu mẫu từ một bài tiểu luận/báo cáo thật.
- Chạy workflow bán thủ công: import source vào Zotero → AI kiểm tra metadata qua CrossRef → AI gợi ý citation format → user review.
- Đo thời gian và số lỗi citation phải sửa.


Exit / rollback:


- Nếu user phải sửa hơn 50% citation trong 2 lần thử → hạ xuống template + Zotero/Mendeley thuần.
- Nếu metadata sai nghiêm trọng → không dùng AI để tự chỉnh reference list.


Decision rationale:


- Problem rõ, workflow rõ, metric rõ.
- Có non-AI components (Zotero/Mendeley).
- AI nằm ở bước kiểm tra metadata và gợi ý format, không ôm toàn bộ workflow.
- Human review rõ ràng.



