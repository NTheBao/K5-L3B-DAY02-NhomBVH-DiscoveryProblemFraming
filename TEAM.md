# Team

> Điền file này trên repo chung do nhóm trưởng fork. Nhóm điền phần **Thông tin nhóm** và **Thành viên**. Mỗi người tự điền phần của mình trong **Cá nhân**. Không copy file này sang repo khác.

## Thông tin nhóm

- Tên nhóm: NhomBVH
- Candidate problem nhóm chọn (1 câu): Khi chuẩn bị nộp bài tập lớn/bài lab môn học trước hạn chót 23h59, sinh viên muốn tự động đối chiếu cấu trúc thư mục, quy tắc đặt tên file và các trường bắt buộc với rubric của đề bài, để không bị trừ điểm oan vì sai format nộp bài.
- Quyết định cuối (Go / Not Yet / No-Go): Go (phạm vi nhỏ: Workflow có AI ở một bước hẹp — Rule làm phần chính, LLM cảnh báo tùy chọn)

## Thành viên

| STT | Họ và tên | MSSV | Vai trò trong nhóm | Tài khoản GitHub |
|---:|---|---|---|---|
| 1 | Nguyễn Thế Bảo | 2A202603825 | Trưởng nhóm, Điều phối thời gian | NTheBao |
| 2 | Phạm Đức Vinh | 2A202603849 | Thành viên nghiên cứu, Phụ trách kiểm chứng | vindpd203 |
| 3 | Vũ Xuân Hiếu | 2A202603860 | Thành viên nghiên cứu, Phản biện chính | vuhieuvh |

Không ghi email hay số điện thoại vào bảng này, vì repo có thể để public.

Gợi ý vai trò (một người có thể giữ nhiều vai): điều phối thời gian, ghi chép, người phản biện chính, phụ trách kiểm chứng (phỏng vấn/survey), phụ trách research, vẽ quy trình, viết Problem Statement.

## Phân công theo checkpoint

| Checkpoint | Người chính | Người hỗ trợ | Sản phẩm |
|---|---|---|---|
| CP3 — Hội tụ nhóm | Vũ Xuân Hiếu | Nguyễn Thế Bảo | Cluster, cây OST, bảng chấm điểm |
| CP4 — Kiểm chứng | Phạm Đức Vinh | Vũ Xuân Hiếu | Assumption map, snapshot hoặc survey |
| CP4 — Research | Nguyễn Thế Bảo | Phạm Đức Vinh | Bảng research có link |
| CP5 — Quy trình trước/sau | Vũ Xuân Hiếu | Nguyễn Thế Bảo | Quy trình + bảng before/after |
| CP5 — Problem Statement v0 | Nguyễn Thế Bảo | Vũ Xuân Hiếu | Problem Statement v0 |
| CP6 — Mức can thiệp + Problem Statement v1 | Vũ Xuân Hiếu | Phạm Đức Vinh | Ma trận, AI Canvas, eval, Problem Statement v1 |
| CP6 — Quyết định | Nguyễn Thế Bảo | Vũ Xuân Hiếu, Phạm Đức Vinh | 4 rủi ro + Go/Not Yet/No-Go |

## Cá nhân

Mỗi thành viên thêm một mục theo mẫu dưới đây, tiêu đề là `HoVaTen-MSSV`.

### VuXuanHieu-2A202603860

**Phần việc phụ trách:**

- Scan các bài toán ban đầu (CP1), soạn 3 Problem Cards (CP2) và pitch bài toán rà soát quy cách nộp bài cho nhóm.
- Tham gia phản biện, đóng góp xây dựng cây OST và kịch bản phỏng vấn The Mom Test.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Đóng góp 10 bài toán scan thực tế đạt điều kiện Bonus B1.
- Soạn thảo Problem Card và vẽ sơ đồ quy trình chi tiết cho bài toán rà soát quy cách nộp bài.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- File cá nhân `report/individual/2A202603860_VuXuanHieu.md`
- Bảng pitch và cây OST trong `report/team/group_report.md`

**Điều mình học được từ phần nhóm:**

- Nhận diện rõ ranh giới giữa một giải pháp công nghệ đơn thuần (Solution) và một cơ hội giải quyết nỗi đau có thật (Opportunity); biết cách dừng lại ở mức can thiệp đơn giản nhất đủ dùng thay vì phức tạp hóa bằng AI.

### PhamDucVinh-2A202603849

**Phần việc phụ trách:**

- Scan 10 bài toán (CP1) và soạn 3 Problem Card (CP2) về hóa đơn điện tử cho kế toán dịch vụ; phản biện card của Bảo và Hiếu ở CP3.
- Người chính phần kiểm chứng CP4; hỗ trợ research CP4 và CP6 (mức can thiệp, chạy eval, quyết định).

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Chấm lại Assumption Map, soạn kịch bản phỏng vấn The Mom Test; tự kiểm từng link trong bảng research 3.3 và bỏ claim không nguồn.
- Đối chiếu quy trình CP5 với `SUBMISSION.md`/`RUBRIC.md`: bổ sung số bước, thời gian bước 6, phương án quay về; bỏ bước tự động commit/push vì trái boundary read-only.
- Chạy thật bộ 10 test case cho bước LLM với một prompt cố định, sửa prompt sau lần chạy nháp báo nhầm (TC-02, TC-10); kết quả 10/10 đạt, dùng làm điều kiện bật bước LLM trong pilot.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- File cá nhân `report/individual/2A202603849_PhamDucVinh.md` (mục 4, 5)
- `report/assets/cp4-interview-script.md`, `report/assets/cp6-eval-run.md`
- Mục 3 (CP4), 4.3 và bảng eval mục 7 trong `report/team/group_report.md`; commit `cf3eab4` (CP3), `734e2bd` (CP4)

**Điều mình học được từ phần nhóm:**

- Card viết kỹ nhất chưa chắc là card nên chọn: tiêu chí "kiểm chứng được ngay" và "nhóm hiểu domain" quan trọng hơn ở giai đoạn Define. Kết quả eval phải chạy thật mới tin được — bản ghi "Đạt" viết sẵn đã che mất hai ca báo nhầm.

### NguyenTheBao-2A202603825

**Phần việc phụ trách:**

- Trưởng nhóm, điều phối thời gian; hỗ trợ CP3, phụ trách research CP4, hỗ trợ quy trình CP5, viết Problem Statement v0 và phụ trách quyết định CP6.
- Pitch 3 Problem Card về theo dõi yêu cầu thay đổi, đối chiếu tài liệu yêu cầu và bug report thiếu thông tin.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Ở CP3, đặt câu hỏi về bằng chứng của candidate paper và tính cần thiết của AI cho kiểm tra quy cách; góp phần giúp nhóm phân biệt phần kiểm tra bằng Rule với phần có thể cần đọc hiểu ngữ nghĩa.
- Ở CP4, tổng hợp research về pre-commit, GitHub Classroom Autograding, Gradescope và markdownlint-cli; rút ra kết luận các bước kiểm tra cấu trúc phần lớn làm được bằng Rule.
- Ở CP5, hỗ trợ hoàn thiện quy trình trước/sau và viết Problem Statement v0; làm rõ metric, boundary read-only và Rule là phương án mặc định.
- Ở CP6, đánh giá bốn rủi ro và đề xuất Go phạm vi nhỏ, pilot 2 bài lab cùng các ngưỡng dừng cho LLM và Rule checker.

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- File cá nhân `report/individual/2A202603825_NguyenTheBao.md` 
- Nguồn research và liên kết được tổng hợp tại  `report/team/group_report.md`.

**Điều mình học được từ phần nhóm:**

- Không nên chọn AI trước khi xác định pain và bằng chứng. Nhiều lỗi quy cách có thể xử lý bằng Rule; vì vậy cần bắt đầu từ mức đơn giản nhất, giữ công cụ read-only và chỉ cân nhắc LLM cho phần Rule không đánh giá được. Các con số chưa có nguồn phải được ghi là giả định và kiểm chứng trước khi dùng làm kết luận.
