# CP6 — Nhật ký chạy bộ eval 10 test case (bước LLM validator)

- Ngày chạy: 09/11/2026
- Người chạy: Phạm Đức Vinh (hỗ trợ CP6 theo phân công trong `TEAM.md`), dùng Claude Code CLI
- Bộ tiêu chí chấm: 5 tiêu chí "Tiêu chí đánh giá đầu ra của bước LLM" ở mục 7 `report/team/group_report.md`
- Kết quả tổng: **10/10 đạt, không ca nào trượt tiêu chí 2 (bịa tiêu chí)** → điều kiện bật bước LLM ở mục 8.2 đã thỏa về mặt eval
- Giới hạn phải ghi rõ: cả 10 ca là dữ liệu mẫu do nhóm tự soạn (đầu vào ngắn, biết trước đáp án). Kết quả này chưa đo hành vi trên bài nộp thật; tỷ lệ cảnh báo nhầm thực tế (≤ 2/10) vẫn phải đo trong pilot theo mục 8.2.

## 1. Chạy nháp và sửa prompt

Trước khi chạy chính thức, chạy nháp cả 10 ca với prompt nháp (chỉ yêu cầu "đối chiếu và cảnh báo nếu chưa đạt", chưa có quy tắc giới hạn phạm vi):

- **TC-10** (Reflection 250 từ): đầu ra có nhận xét *"nội dung khá chung chung, nên bổ sung ví dụ cụ thể"* — là nhận xét chất lượng ngoài phạm vi quy cách, sẽ trượt tiêu chí 5 nếu tính.
- **TC-02** (Success Metric có đủ 3 phần): đầu ra có câu *"mẫu 2 bài lab còn nhỏ, nên mở rộng cách đo"* — báo nhầm ngoài phạm vi (cách đo đã có trong mục).
- 8 ca còn lại cho đầu ra trùng với lần chạy chính thức.

**Đã sửa prompt:** bổ sung Quy tắc 3 (cấm nhận xét chất lượng ngoài phạm vi) và Quy tắc 4 (mục không thuộc danh sách được chỉ định thì chỉ báo "ngoài phạm vi", không nhận xét gì thêm), rồi chạy lại đủ 10 ca với prompt chốt ở mục 2. Kết quả dưới đây là của lần chạy chính thức với prompt chốt này.

## 2. Prompt cố định dùng cho lần chạy chính thức

Chạy từng ca một, chỉ thay đổi "MỤC ĐƯỢC CHỈ ĐỊNH" và "NỘI DUNG"; không đổi phần còn lại:

```text
Bạn là bước kiểm tra nội dung (LLM validator) trong quy trình kiểm tra quy cách bài nộp
của nhóm. Rule checker đã chạy xong và tách cho bạn MỘT mục được chỉ định. Nhiệm vụ:
đối chiếu nội dung mục đó với các đoạn trích yêu cầu được cung cấp và quyết định cảnh
báo hay không.

QUY TẮC BẮT BUỘC:
1. Mỗi cảnh báo phải trích NGUYÊN VĂN một yêu cầu nằm trong "Đoạn trích yêu cầu" dưới
   đây, kèm tên file và mục. Không được nêu tiêu chí không có trong đoạn trích.
2. Chỉ cảnh báo lỗi thuộc phạm vi quy cách: Success Metric thiếu baseline/target/cách đo;
   Job Story hoặc Problem Statement lẫn giải pháp; Boundary không nêu AI không được làm
   gì hoặc khi nào con người kiểm tra; câu hỏi phỏng vấn dạng "Bạn có muốn…".
3. KHÔNG chấm điểm, KHÔNG nhận xét chất lượng nội dung ngoài phạm vi trên (ví dụ
   "chung chung", "nên viết hay hơn", "mẫu còn nhỏ").
4. Nếu mục đã đủ yêu cầu theo đoạn trích: trả lời KHÔNG CẢNH BÁO kèm một dòng nêu phần
   nào thỏa. Nếu mục không thuộc danh sách mục được chỉ định: trả lời KHÔNG CẢNH BÁO và
   ghi "ngoài phạm vi bước LLM", không nhận xét gì thêm.
5. Không đề xuất cách sửa, không viết lại nội dung.

ĐOẠN TRÍCH YÊU CẦU (nguồn duy nhất được phép trích):
[CP1-1] CHECKPOINTS.md, CP1: "Viết mỗi problem theo mẫu Job Story: Khi [tình huống],
        tôi muốn [động cơ], để [kết quả]."
[CP1-2] CHECKPOINTS.md, CP1 tự kiểm tra: "Không dòng nào có chữ "AI", "chatbot", "agent"
        trong cột Job Story (kể cả dòng thuộc lăng kính "Cần đọc, tổng hợp nhiều thông
        tin": mô tả việc khó, chưa nói cách giải)."
[WS-1] docs/01-worksheet.md, CP1: "Job Story ép bạn ghi tình huống (khi nào xảy ra) và
        kết quả (vì sao quan trọng). Nó cũng ngăn bạn viết giải pháp vào phần problem."
[CP5-1] CHECKPOINTS.md, CP5: "Success Metric phải có baseline (hiện tại là bao nhiêu),
        target (muốn đạt bao nhiêu) và cách đo. "Nhanh hơn", "tiện hơn" không phải metric."
[CP5-2] CHECKPOINTS.md, CP5 tự kiểm tra: "Boundary ghi rõ AI không được làm gì và khi nào
        cần con người kiểm tra (HITL — human-in-the-loop)."
[WS-2] docs/01-worksheet.md, CP5: "Problem Statement không chứa giải pháp. Nó mô tả đủ
        rõ để nhiều giải pháp khác nhau có thể được thử."
[WS-3] docs/01-worksheet.md, CP4 (Mom Test): "❌ Đừng hỏi: Bạn có muốn một công cụ AI
        viết báo cáo không?" · "Hỏi về chuyện cụ thể đã xảy ra, không hỏi chung chung
        hay giả định về tương lai."
[R-C7] RUBRIC.md, C7: "Câu hỏi dạng "Bạn có muốn…": trừ 3."

MỤC ĐƯỢC CHỈ ĐỊNH: <Success Metric | Job Story | Boundary | Problem Statement | Câu hỏi phỏng vấn>
NỘI DUNG: <văn bản mục>

ĐỊNH DẠNG TRẢ LỜI:
Kết luận: CẢNH BÁO | KHÔNG CẢNH BÁO
Lý do: 1–2 câu
Căn cứ: trích nguyên văn yêu cầu + mã đoạn trích
Vị trí: tên mục bị xét
```

## 3. Kết quả từng ca (đầu ra thật của lần chạy chính thức)

Chấm theo 5 tiêu chí ở mục 7 báo cáo nhóm: (1) Có căn cứ, (2) Không bịa tiêu chí, (3) Bắt được mục chưa đạt, (4) Không báo nhầm mục đã đạt, (5) Giữ đúng phạm vi.

| Test # | Đầu vào (tóm tắt) | Đầu ra thật của bước LLM | Chấm tiêu chí nhóm | Kết luận |
|---:|---|---|---|---|
| TC-01 | Success Metric: *"Giúp sinh viên làm bài nhanh hơn và tiện hơn"* | **CẢNH BÁO** — Lý do: không có baseline, không có target, không có cách đo; "nhanh hơn và tiện hơn" đúng dạng mà yêu cầu tuyên bố không tính là metric. Căn cứ [CP5-1] (trích nguyên văn kèm tên file CHECKPOINTS.md, CP5). Vị trí: Success Metric | 1 ✓ (có căn cứ, ghi file + mục) · 3 ✓ (bắt đủ 3 phần thiếu) · 2 ✓ (căn cứ khớp nguyên văn [CP5-1]) | **Đạt** |
| TC-02 | Success Metric: *"Thời gian rà soát từ 20 phút xuống dưới 5 phút, đo bằng bấm giờ 2 bài lab"* | **KHÔNG CẢNH BÁO** — đủ cả 3 phần: baseline "20 phút", target "dưới 5 phút", cách đo "bấm giờ 2 bài lab" ([CP5-1] thỏa) | 4 ✓ (không báo nhầm mục đã đủ) | **Đạt** |
| TC-03 | Success Metric: *"Giảm từ 6/30 bài lỗi xuống 1/30"* | **CẢNH BÁO** — có baseline (6/30) và target (1/30) nhưng thiếu cách đo. Căn cứ [CP5-1]. Vị trí: Success Metric | 1 ✓ · 3 ✓ · 2 ✓ | **Đạt** |
| TC-04 | Job Story: *"Khi làm bài lab, tôi muốn có chatbot AI để làm hộ bài"* | **CẢNH BÁO** — Job Story chứa chữ "AI", "chatbot" và mô tả giải pháp ("làm hộ bài"). Căn cứ [CP1-2] và [CP1-1] ("tôi muốn [động cơ]" — "chatbot AI làm hộ bài" là giải pháp, không phải động cơ). Vị trí: Job Story | 1 ✓ · 3 ✓ · 2 ✓ | **Đạt** |
| TC-05 | Job Story: *"Khi chuẩn bị báo cáo, tôi muốn có một công cụ tự động tóm tắt tài liệu, để tiết kiệm thời gian"* (không có từ "AI", "chatbot") | **CẢNH BÁO** — "tôi muốn có một công cụ tự động tóm tắt tài liệu" là tên công cụ/giải pháp, không phải động cơ. Căn cứ [WS-1] ("Nó cũng ngăn bạn viết giải pháp vào phần problem") và [CP1-1]. Vị trí: Job Story | 3 ✓ (bắt được giải pháp dù không có từ khóa AI — ca khó nhất) · 2 ✓ (căn cứ khớp nguyên văn [WS-1]) | **Đạt** |
| TC-06 | Boundary: *"AI sẽ hỗ trợ người dùng một cách tốt nhất"* | **CẢNH BÁO** — chỉ là cam kết chung; không nêu AI không được làm gì, không nêu khi nào con người kiểm tra. Căn cứ [CP5-2]. Vị trí: Boundary | 1 ✓ · 3 ✓ · 2 ✓ | **Đạt** |
| TC-07 | Boundary: *"AI không tự gửi, không tự sửa số liệu; PM duyệt trước khi gửi"* | **KHÔNG CẢNH BÁO** — nêu rõ AI không được làm gì ("không tự gửi, không tự sửa số liệu") và bước con người kiểm tra ("PM duyệt trước khi gửi") ([CP5-2] thỏa) | 4 ✓ | **Đạt** |
| TC-08 | Problem Statement v0 có dòng *"Giải pháp: dùng LLM đọc rubric và chấm bài"* | **CẢNH BÁO** — Problem Statement chứa giải pháp. Căn cứ [WS-2] ("Problem Statement không chứa giải pháp"). Vị trí: Problem Statement v0 | 1 ✓ · 3 ✓ · 2 ✓ | **Đạt** |
| TC-09 | Câu hỏi phỏng vấn: *"Bạn có muốn dùng một công cụ kiểm tra tự động không?"* | **CẢNH BÁO** — câu hỏi dạng "Bạn có muốn…", hỏi về ý tưởng thay vì chuyện cụ thể đã xảy ra. Căn cứ [R-C7] (RUBRIC.md, C7 — nguyên văn "Câu hỏi dạng "Bạn có muốn…": trừ 3") và [WS-3]. Vị trí: Câu hỏi phỏng vấn | 1 ✓ · 2 ✓ (cả 2 căn cứ đều nguyên văn có trong file) · 3 ✓ | **Đạt** |
| TC-10 | Reflection 6.1 dài 250 từ, trải nghiệm thật | **KHÔNG CẢNH BÁO** — "ngoài phạm vi bước LLM": Reflection không thuộc danh sách mục được chỉ định; kiểm số từ tối thiểu là việc của Rule checker. Không đưa nhận xét chất lượng nội dung (Quy tắc 3, 4 của prompt) | 5 ✓ (giữ đúng phạm vi) | **Đạt** |

## 4. Kiểm tiêu chí 2 (không bịa tiêu chí)

Mã căn cứ xuất hiện ở mục 3: [CP5-1] (TC-01, 02, 03), [CP1-2] (TC-04), [CP1-1] (TC-04, 05), [WS-1] (TC-05), [CP5-2] (TC-06, 07), [WS-2] (TC-08), [R-C7] (TC-09), [WS-3] (TC-09). Đối chiếu từng mã với đoạn trích trong prompt (mục 2), nguồn gốc là `CHECKPOINTS.md`, `docs/01-worksheet.md`, `RUBRIC.md` trong repo: **tất cả khớp nguyên văn, không có cảnh báo nào dùng tiêu chí ngoài các đoạn trích** → 0 ca trượt tiêu chí 2.

## 5. Kết luận

1. Điều kiện "≥ 8/10 và không ca nào trượt tiêu chí 2" ở mục 8.2 báo cáo nhóm: **thỏa** (10/10, 0 ca trượt tiêu chí 2) — bước LLM được phép bật ở pilot, với điều kiện đo lại tỷ lệ cảnh báo nhầm trên bài nộp thật (≤ 2/10).
2. Bài học từ chạy nháp: lỗi thật của bước LLM không phải "bịa căn cứ" mà là **báo nhầm ngoài phạm vi** (nhận xét chất lượng viết, nghi ngờ mẫu nhỏ) — đúng loại rủi ro nhóm dự đoán ở mục 6.4 (PAIR: báo nhầm nhiều làm người dùng bỏ qua cảnh báo đúng). Prompt chốt phải giữ nguyên Quy tắc 3–4 khi chạy pilot.
3. Hạn chế đã ghi ở mục 5 báo cáo nhóm: bộ eval là dữ liệu mẫu tự soạn; chưa thay thế được đo trên bài nộp thật trong pilot.
