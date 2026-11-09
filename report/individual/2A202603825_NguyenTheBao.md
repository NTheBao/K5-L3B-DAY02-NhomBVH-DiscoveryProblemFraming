# Báo cáo cá nhân — 2A202603825

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Nguyễn Thế Bảo
- MSSV: 2A202603825
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: Nhóm BVH
- Link repo nhóm: https://github.com/NTheBao/K5-L3B-DAY02-NhomBVH-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Lặp lại |Khi nhận yêu cầu chỉnh sửa từ khách hàng nhiều lần, tôi muốn theo dõi các thay đổi, để tránh bỏ sót yêu cầu | Dev, BA | 2-3 lần thay đổi/tuần |
| 2 | Pain từ người khác |Khi khách hàng không biết cách mô tả yêu cầu kỹ thuật, tôi muốn hiểu chính xác vấn đề họ đang gặp phải, để tránh phát triển sai chức năng | Khách hàng, Dev | 1-2 lần/yêu cầu |
| 3 | Tốn thời gian | Khi phải tìm nguyên nhân của một lỗi khó, tôi muốn xác định phạm vi cần kiểm tra, để giảm thời gian xử lý lỗi | Dev | Số giờ/bug |
| 4 | Tốn thời gian | Khi phải giải thích một tính năng cho khách hàng không có chuyên môn kỹ thuật, tôi muốn giải thích dễ hiểu, để khách hàng nắm được phạm vi công việc. | Dev, BA | 2 lần/tháng |
| 5 | Cần đọc, tổng hợp nhiều thông tin | Khi khách hàng thay đổi yêu cầu qua nhiều cuộc họp, tôi muốn đối chiếu yêu cầu ban đầu và yêu cầu mới, để xác định chính xác những điểm thay đổi | BA | Số điểm thay đổi/dự án |
| 6 | Lặp lại | Khi bàn giao dự án, tôi muốn kiểm tra đầy đủ các hạng mục bàn giao, để hạn chế thiếu tài liệu hoặc thông tin. | Dev | Số hạng mục/dự án |
| 7 | Lặp lại | Khi phải kiểm tra các chức năng giống nhau ở nhiều phiên bản, tôi muốn tránh lặp lại thao tác kiểm tra, để tiết kiệm thời gian. | Tester | Số giờ/tuần |
| 8 | Pain từ người khác | Khi Tester phát hiện lỗi nhưng mô tả chưa đủ thông tin, tôi muốn có đầy đủ dữ liệu tái hiện lỗi, để xử lý chính xác. | Tester, Dev | thời gian bổ sung/bug |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

- Bỏ xây dựng AI hỗ trợ lập trình vì tốn kém, khó đánh giá hiệu quả

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 |Theo dõi yêu cầu chỉnh sửa từ khách hàng: Khi nhận yêu cầu chỉnh sửa từ khách hàng nhiều lần, tôi muốn theo dõi các thay đổi, để tránh bỏ sót yêu cầu | Xảy ra thường xuyên (ước tính 2–3 lần/tuần) | Chưa xác định chính xác số yêu cầu |
| 2 | Đối chiếu yêu cầu qua nhiều cuộc họp: Khi khách hàng thay đổi yêu cầu qua nhiều cuộc họp, tôi muốn đối chiếu yêu cầu ban đầu và yêu cầu mới, để xác định chính xác những điểm thay đổi |BA phải tổng hợp thông tin từ nhiều cuộc họp và tài liệu. Nếu bỏ sót thay đổi, nhóm phát triển có thể thực hiện theo yêu cầu cũ | Chưa rõ trung bình mỗi dự án có bao nhiêu điểm thay đổi và mất bao nhiêu phút để đối chiếu |
| 3 | ổ sung thông tin lỗi từ Tester: Khi Tester phát hiện lỗi nhưng mô tả chưa đủ thông tin, tôi muốn có đầy đủ dữ liệu tái hiện lỗi, để xử lý chính xác | Developer thường phải trao đổi lại với Tester, gây gián đoạn công việc và kéo dài thời gian sửa lỗi | Chưa xác định tỷ lệ bug thiếu thông tin trên tổng số bug và thời gian trung bình bổ sung thông tin |

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi nhận yêu cầu chỉnh sửa từ khách hàng nhiều lần, tôi muốn theo dõi các thay đổi, để tránh bỏ sót yêu cầu|
| Actor | Dev, BA |
| Thời điểm / bối cảnh | Khi khách hàng gửi yêu cầu chỉnh sửa qua email, tin nhắn hoặc trong các cuộc họp. |
| Quy trình hiện tại (3–7 bước) | 1. Khách hàng gửi yêu cầu thay đổi.2. BA/Dev tiếp nhận thông tin.3. Đọc và xác định nội dung thay đổi.4. Ghi nhận yêu cầu vào tài liệu hoặc công cụ quản lý công việc.5. Thông báo cho các thành viên liên quan.6. Dev thực hiện chỉnh sửa theo yêu cầu. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3–4: Phải đọc lại nhiều nguồn thông tin và cập nhật thủ công. Thời gian ước tính: 10–20 phút/lần thay đổi, cần đo thực tế |
| Impact (nếu không giải thì sao) | 	Bỏ sót yêu cầu, phát triển sai chức năng, phải chỉnh sửa lại, ảnh hưởng tiến độ và tăng chi phí dự án |
| Success metric (baseline → target) | Thời gian ghi nhận một thay đổi: 10–20 phút → giảm ít nhất 30%.
Số yêu cầu bị bỏ sót: đo baseline → giảm ít nhất 50% |
| Phương án không dùng AI | Sử dụng biểu mẫu ghi nhận yêu cầu, bảng theo dõi thay đổi và công cụ quản lý công việc |
| Giả thuyết về AI (nếu có) | 	AI có thể đọc nội dung trao đổi, trích xuất yêu cầu thay đổi, tóm tắt điểm mới và hỗ trợ đối chiếu với yêu cầu trước đó |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:

```
HIỆN TẠI — ƯỚC TÍNH 45–75 phút/lần thay đổi
[1 Khách hàng gửi yêu cầu: 5'] → [2 BA/Dev tiếp nhận: 5']
→ [3 Đọc và xác định nội dung thay đổi: 10–20'] ← BOTTLENECK
→ [4 Ghi nhận vào tài liệu/công cụ quản lý: 10–20']
→ [5 Thông báo thành viên liên quan: 5']
→ [6 Dev thực hiện chỉnh sửa: 10–20']
```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | 	Khi khách hàng thay đổi yêu cầu qua nhiều cuộc họp, tôi muốn đối chiếu yêu cầu ban đầu và yêu cầu mới, để xác định chính xác những điểm thay đổi|
| Actor | BA |
| Thời điểm / bối cảnh | Sau các cuộc họp trao đổi với khách hàng, khi có nhiều phiên bản tài liệu yêu cầu hoặc biên bản họp |
| Quy trình hiện tại (3–7 bước) |1. Thu thập tài liệu yêu cầu ban đầu.2. Ghi nhận nội dung từ các cuộc họp mới.3. Tổng hợp yêu cầu mới vào tài liệu.4. Mở và đọc các phiên bản tài liệu khác nhau.5. So sánh nội dung cũ và mới.6. Xác định các điểm thay đổi.7. Thông báo cho Dev và các bên liên quan. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 4–5: BA phải đọc và so sánh nhiều tài liệu thủ công. Thời gian ước tính: 30–60 phút/lần đối chiếu, cần đo thực tế |
| Impact (nếu không giải thì sao) | Không phát hiện đầy đủ các thay đổi, đội ngũ phát triển có thể sử dụng yêu cầu cũ, dẫn đến sai chức năng và phát sinh công việc sửa chữa |
| Success metric (baseline → target) | Thời gian đối chiếu tài liệu: 30–60 phút/lần → giảm ít nhất 40%.
Tỷ lệ điểm thay đổi được phát hiện: đo baseline → đạt ít nhất 95%. |
| Phương án không dùng AI | Sử dụng chức năng Compare của Microsoft Word, theo dõi phiên bản tài liệu và lập bảng so sánh yêu cầu |
| Giả thuyết về AI (nếu có) | AI có thể đọc nhiều phiên bản tài liệu, nhận diện nội dung được thêm, sửa hoặc xóa, sau đó tạo bản tổng hợp các điểm thay đổi để BA kiểm tra |
| Cảm nhận nhanh | AI |

Quy trình nháp hiện tại:

```
HIỆN TẠI — ƯỚC TÍNH 60–100 phút/lần đối chiếu
[1 Thu thập tài liệu ban đầu: 5'] → [2 Ghi nhận yêu cầu mới: 10']
→ [3 Tổng hợp tài liệu mới: 10']
→ [4 Mở và đọc các phiên bản tài liệu: 15–25']
→ [5 So sánh nội dung cũ và mới: 30–60'] ← BOTTLENECK
→ [6 Xác định điểm thay đổi: 5']
→ [7 Thông báo Dev và các bên liên quan: 5']
```

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi Tester phát hiện lỗi nhưng mô tả chưa đủ thông tin, tôi muốn có đầy đủ dữ liệu tái hiện lỗi, để xử lý chính xác và giảm thời gian trao đổi qua lại. |
| Actor | Tester, Dev |
| Thời điểm / bối cảnh | Khi Tester tạo bug report và chuyển lỗi cho Dev xử lý trong quá trình kiểm thử phần mềm. |
| Quy trình hiện tại (3–7 bước) | 	1. Tester thực hiện kiểm thử chức năng.2. Phát hiện lỗi trong quá trình kiểm thử.3. Tạo bug report và mô tả lỗi.4. Chuyển bug report cho Dev.5. Dev đọc mô tả và kiểm tra lỗi.6. Nếu thiếu thông tin, Dev liên hệ Tester để hỏi thêm.7. Tester bổ sung thông tin và Dev tiếp tục xử lý. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 5–6: Dev phải trao đổi lại với Tester để lấy thông tin còn thiếu. Thời gian ước tính: 10–15 phút/bug cho việc trao đổi bổ sung, cần đo thực tế |
| Impact (nếu không giải thì sao) | Thời gian xử lý bug kéo dài, Dev khó tái hiện lỗi, việc phối hợp giữa Tester và Dev kém hiệu quả, ảnh hưởng tiến độ kiểm thử |
| Success metric (baseline → target) |Thời gian bổ sung thông tin: 10–15 phút/bug → giảm ít nhất 50%.
Tỷ lệ bug report thiếu thông tin: đo baseline → giảm ít nhất 50%. |
| Phương án không dùng AI | Tạo mẫu bug report bắt buộc có các trường: môi trường kiểm thử, bước tái hiện, kết quả mong đợi, kết quả thực tế, mức độ nghiêm trọng và ảnh chụp màn hình |
| Giả thuyết về AI (nếu có) | AI có thể kiểm tra nội dung bug report, phát hiện trường thông tin còn thiếu và gợi ý câu hỏi để Tester bổ sung trước khi chuyển cho Dev |
| Cảm nhận nhanh | Rule + Workflow|

Quy trình nháp hiện tại:

```
HIỆN TẠI — ƯỚC TÍNH 20–35 phút/bug (khi phải bổ sung thông tin)
[1 Tester thực hiện kiểm thử: 5'] → [2 Phát hiện lỗi: 2']
→ [3 Tạo Bug Report: 5–10']
→ [4 Chuyển Bug Report cho Dev: 1']
→ [5 Dev đọc và kiểm tra lỗi: 2–3']
→ [6 Trao đổi để bổ sung thông tin: 10–15'] ← BOTTLENECK
→ [7 Tester bổ sung thông tin và Dev tiếp tục xử lý: 5']
```

### Card muốn pitch nhất

- Card số: 2
- Vì sao:BA thường phải đọc nhiều tài liệu và biên bản họp để xác định những điểm khách hàng đã thay đổi. Việc so sánh thủ công tốn thời gian và có nguy cơ bỏ sót thông tin
- Câu hỏi muốn nhóm phản biện: AI có thực sự cần thiết cho công việc này không, hay chỉ cần sử dụng chức năng Compare trong Microsoft Word? Làm thế nào để đảm bảo AI không bỏ sót hoặc hiểu sai những thay đổi về yêu cầu nghiệp vụ?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Chưa xác định rõ nguồn tài liệu đầu vào để đối chiếu | Có | Xác định đầu vào gồm tài liệu yêu cầu ban đầu, tài liệu cập nhật và biên bản họp |
| Chưa chứng minh AI tốt hơn công cụ Compare có sẵn  | Có | Bổ sung phương án không dùng AI là Microsoft Word Compare; cần thử nghiệm và so sánh thời gian, độ chính xác giữa hai phương án |
| Có nguy cơ lộ thông tin khách hàng khi đưa tài liệu lên AI | Có | Bổ sung yêu cầu sử dụng dữ liệu đã được cho phép, ẩn thông tin nhạy cảm và tuân thủ chính sách bảo mật của doanh nghiệp |
---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Pitch 3 card cho Dev/BA/Tester: #7 theo dõi yêu cầu chỉnh sửa của khách hàng, #8 đối chiếu yêu cầu qua nhiều cuộc họp (card muốn pitch nhất), #9 bug report thiếu thông tin | Card #9 được đưa vào shortlist (25/35); #7 và #8 bị loại vì thiếu bằng chứng thật, #8 còn vướng bảo mật tài liệu khách hàng |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: hỏi Hiếu (#1) "Viết shell script hay Python regex là kiểm tra được, sao cần AI?"; hỏi Hiếu (#3) "Tỷ lệ sai 25% đo từ 4 buổi seminar, mẫu có quá nhỏ không? Kiểm chứng trong một buổi lab bằng cách nào?"; hỏi Vinh (#5) "Phần mềm kế toán đang dùng đã có chức năng lấy hóa đơn hàng loạt từ cơ quan thuế chưa?" | Câu hỏi cho #1 dẫn tới hướng "Rule (cấu trúc) trước, chỉ thêm AI (nội dung) nếu Rule không đủ", được giữ đến CP6; câu hỏi cho #3 và #5 góp phần loại hai card này |
| Nhận phản biện | Câu hỏi tôi nhận được: Vinh hỏi (#7) lần bỏ sót yêu cầu gần nhất và con số 2–3 lần/tuần có ghi chép không; Vinh hỏi (#9) chỉ dùng template bug report bắt buộc là đủ chưa; Hiếu hỏi (#8) "Word Compare đã làm được việc này, AI thêm được gì? Tài liệu khách hàng có được phép đưa lên AI không?" | Tôi đã sửa gì: **[cần xác nhận]** — gợi ý: thừa nhận số liệu #9 là ước tính, chưa có baseline (Pain 2/5); ghi Word Compare là phương án No AI và thêm yêu cầu bảo mật cho #8 (khớp bảng "AI đã phản biện card" mục 3) |
| Gom cluster / cây OST | Người hỗ trợ CP3 (theo `TEAM.md`) **[cần xác nhận việc cụ thể]** | **[cần xác nhận]** |
| Chọn candidate problem | Ban đầu cho rằng #1 chỉ cần một script Bash/Python, không cần AI | Nhóm thống nhất script kiểm được tên file, cấu trúc thư mục nhưng không kiểm được mục bắt buộc đã điền thật hay còn template; chọn #1 với hướng Rule trước, để CP6 quyết định có cần AI không |
| Kiểm chứng / research | Người chính phần research CP4 (theo `TEAM.md`): bảng giải pháp đã có (pre-commit, GitHub Classroom Autograding, Gradescope, markdownlint-cli) **[cần xác nhận phần nào do Bảo tìm]**; commit "4 commit" | Kết luận research: công cụ có sẵn và vài script Rule đã giải phần lớn bước 2–3; khoảng trống còn lại là lớp không dùng GitHub Classroom và phần kiểm tra nội dung |
| Quy trình nhóm | Người hỗ trợ CP5 quy trình trước/sau (theo `TEAM.md`) **[cần xác nhận việc cụ thể]** | **[cần xác nhận]** |
| Problem Statement | Người chính viết Problem Statement v0 (theo `TEAM.md`); commit "cp5 commit" | **[cần xác nhận]** — gợi ý: v0 là bản nền, sau phản biện thì sửa Impact theo `RUBRIC.md` và target ≤ 1/30 bài |
| Mức can thiệp AI | **[cần xác nhận]** — `TEAM.md` không giao CP6 mức can thiệp cho Bảo | |
| Quyết định | Người chính phần quyết định CP6 (theo `TEAM.md`): đánh giá 4 rủi ro và chọn Go / Not Yet / No-Go **[cần xác nhận]** | Go phạm vi nhỏ, pilot 2 bài lab, có ngưỡng dừng (mục 8.2) |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Sau khi tự viết 8 problem từ trải nghiệm của mình, tôi dùng AI để gợi ý thêm các góc nhìn cho phần scan. | AI có thể nhắc đến những tình huống tôi chưa nghĩ tới. | Gợi ý dễ chung chung hoặc chuyển sang đề xuất giải pháp, chẳng hạn ý tưởng xây AI hỗ trợ lập trình, trong khi chưa có dấu hiệu thực tế hay cách đo phù hợp. | Tôi không giữ ý chỉ vì AI đề xuất; loại ý xây AI hỗ trợ lập trình vì tốn kém, khó đánh giá hiệu quả, và ưu tiên problem có bối cảnh cùng dấu hiệu kiểm chứng được. |
| CP2 Problem Card | Tôi nhờ AI phản biện card bug report thiếu thông tin, tập trung vào actor, quy trình, bottleneck, metric và phương án không dùng AI. | AI giúp chỉ ra các điểm cần làm rõ và nhắc tôi xem xét liệu một mẫu bug report có thể giải quyết vấn đề hay không. | Nhận xét và số phút ước tính của AI không có dữ liệu thực tế để xác nhận; phản biện chưa chứng minh rằng giả thuyết AI tốt hơn một mẫu có trường bắt buộc. | Tôi ghi rõ thời gian là ước tính, chưa có baseline; bổ sung mẫu bug report bắt buộc các trường làm phương án No AI và không xem lợi ích AI là sự thật đã được kiểm chứng. |
| CP4 Research | Tôi phụ trách research giải pháp có sẵn; không dùng AI thay cho phỏng vấn hoặc xác nhận dữ kiện. | Không áp dụng: tôi dựa vào các nguồn trong bảng research để xem xét giải pháp hiện có. | Không có đầu ra AI nào được dùng làm bằng chứng kiểm chứng problem; nhận định không có nguồn không đủ cơ sở để kết luận. | Tôi phân biệt thông tin có nguồn với giả định và không dùng research thay cho kết quả phỏng vấn của nhóm. |
| CP5 Quy trình | Tôi hỗ trợ đối chiếu quy trình trước/sau với yêu cầu bài và boundary của nhóm; không dùng AI trực tiếp để quyết định các bước. | Không áp dụng: nhóm thống nhất phần kiểm tra theo Rule và phần cần con người xử lý dựa trên quy trình, boundary đã chọn. | Không có đầu ra AI được dùng làm căn cứ cho quy trình; tự động hóa vượt boundary read-only sẽ không phù hợp. | Tôi giữ quy trình read-only: công cụ chỉ kiểm tra/cảnh báo, người học tự sửa và tự nộp bài. |
| CP5–6 Problem Statement | Tôi tự viết Problem Statement v0 và rà soát bằng phản biện cùng bằng chứng nhóm thu thập được; không dùng AI viết thay. | Không áp dụng: việc tách problem khỏi giải pháp dựa trên phản biện của nhóm và nội dung rubric. | Chưa có bằng chứng thực tế để khẳng định LLM là cần thiết hoặc các con số giả định là baseline. | Tôi giữ số chưa kiểm chứng ở dạng giả định, đối chiếu với rubric và bằng chứng nhóm có, không biến đề xuất thành dữ kiện. |
| CP6 Mức can thiệp / quyết định | Tôi tham gia quyết định mức can thiệp và các rủi ro; tham khảo kết quả eval do thành viên khác thực hiện, không tự chạy eval. | Eval cung cấp thêm căn cứ để cân nhắc một bước LLM hẹp trong workflow, bên cạnh phần Rule. | Kết quả AI không tự chứng minh cách làm an toàn hay đủ chính xác; cần xem tiêu chí, ca kiểm thử và boundary. | Tôi giữ quyết định Go ở phạm vi nhỏ: Rule làm phần chính, LLM chỉ là bước tùy chọn và chỉ bật khi đạt điều kiện eval; công cụ không tự sửa hay tự nộp bài. |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**
Khi nghe phần trình bày của Hiếu và Vinh, tôi nhận ra mỗi người có cách nhìn nhận vấn đề khác nhau. Hiếu tập trung vào việc kiểm tra quy cách bài nộp theo rubric, còn Vinh tập trung vào quy trình xử lý hóa đơn điện tử và đối chiếu dữ liệu kế toán. Qua đó, tôi học được rằng một vấn đề tốt không nhất thiết phải có giải pháp công nghệ phức tạp mà quan trọng là phải có nỗi đau thực tế, đối tượng chịu ảnh hưởng rõ ràng và có thể kiểm chứng được

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**
Có. Trong quá trình thảo luận, nhóm tôi đã có lúc nghĩ đến giải pháp trước khi phân tích đầy đủ vấn đề. Khi Hiếu trình bày bài toán kiểm tra quy cách bài nộp, tôi nhanh chóng nghĩ đến việc xây dựng bot Discord, còn Hiếu sử dụng LLM đọc rubric hoặc viết script tự động kiểm tra file, Vinh thì nghĩ đến việc tích hợp thẳng vào GitHub Actions để tự sửa bài.
Tuy nhiên,nhóm nhận ra rằng các ý tưởng trên đều là giải pháp chứ không phải vấn đề của người dùng. Nhóm đã quay lại phân tích hành vi thực tế của sinh viên, đặc biệt là việc phải kiểm tra thủ công tên file, thư mục và nội dung bắt buộc trong thời gian sát deadline. Từ đó, nhóm tập trung vào nỗi đau chính là sinh viên dễ bỏ sót lỗi định dạng khi tự rà soát bài. Tôi học được rằng cần hiểu rõ nguyên nhân và quy trình trước khi quyết định sử dụng công nghệ nào.

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**
Có. Một lần cụ thể là khi nhóm thảo luận về problem card của Hiếu. Ban đầu, tôi cho rằng có thể sử dụng AI để kiểm tra toàn bộ bài nộp vì AI có khả năng đọc hiểu nội dung và phát hiện nhiều lỗi. Tuy nhiên, khi phân tích kỹ hơn, tôi nhận ra những lỗi như sai tên file, sai tên thư mục hoặc thiếu file hoàn toàn có thể kiểm tra bằng Python, Bash script hoặc các quy tắc cố định.

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**
Có. Điều khiến tôi bất ngờ nhất là kết quả phỏng vấn trợ giảng (TA). Ban đầu, nhóm cho rằng việc kiểm tra quy cách bài nộp cần một công cụ AI để tự động phân tích và phát hiện lỗi. Tuy nhiên, qua trao đổi, nhóm biết rằng trợ giảng đã có script Bash để kiểm tra những lỗi định dạng cố định. Điều đó cho thấy vấn đề không hẳn nằm ở việc thiếu công nghệ mà nằm ở việc sinh viên chưa có công cụ tương tự để tự kiểm tra bài trước khi nộp. Một điều bất ngờ khác là người dùng không muốn AI tự động sửa file vì lo ngại nội dung ban đầu bị thay đổi. Họ chỉ muốn công cụ chỉ ra lỗi để tự quyết định cách sửa. Những kết quả này khiến nhóm thay đổi hướng thiết kế, ưu tiên chế độ chỉ đọc (Read-only) và hỗ trợ người dùng thay vì tự động thực hiện mọi thao tác

**6.5. Điều khó nhất khi viết Problem Statement là gì?**
Theo tôi, điều khó nhất là xác định đúng phạm vi vấn đề và đưa ra các số liệu có căn cứ. Ban đầu, nhóm có xu hướng đưa ra những mục tiêu khá cao như giảm hoàn toàn lỗi định dạng hoặc tiết kiệm phần lớn thời gian kiểm tra. Tuy nhiên, khi đối chiếu với rubric và kết quả phỏng vấn, chúng tôi nhận ra rằng những con số đó chưa có đủ bằng chứng. Nhóm phải điều chỉnh lại các metric để có thể đo lường thực tế hơn, chẳng hạn sử dụng mốc 6/30 bài sai quy cách và đặt mục tiêu giảm xuống tối đa 1/30 bài.

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**
Nếu được làm lại, tôi sẽ đề xuất nhóm thực hiện phỏng vấn người dùng sớm hơn, ngay từ CP2, thay vì đợi đến CP4 mới kiểm chứng các giả định. Điều này sẽ giúp nhóm tiết kiệm thời gian và tránh phát triển những ý tưởng dựa trên suy đoán cá nhân. Tôi cũng sẽ phản biện mạnh hơn về sự cần thiết của AI trong từng bước của quy trình. Cụ thể, tôi muốn nhóm chứng minh rõ AI mang lại giá trị gì so với các giải pháp Rule-based đã có. Nếu chỉ kiểm tra tên file, cấu trúc thư mục hoặc sự tồn tại của tài liệu thì không cần thiết phải sử dụng LLM. Ngoài ra, tôi sẽ yêu cầu nhóm đưa ra bằng chứng cho từng metric ngay từ đầu, tránh sử dụng các con số ước lượng nhưng chưa được kiểm chứng. Qua bài tập này, tôi hiểu rằng một giải pháp tốt không phải là giải pháp sử dụng công nghệ tiên tiến nhất mà là giải pháp phù hợp nhất với nhu cầu thực tế của người dùng.

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.
1. Problem: Sinh viên thường gặp khó khăn khi kiểm tra quy cách bài nộp trước deadline 23h59, dễ sai tên file, tên thư mục hoặc để sót nội dung bắt buộc trong template.
2. Quy trình: Nhóm đề xuất quy trình kiểm tra hai tầng, trong đó Rule Engine kiểm tra cấu trúc file và LLM Validator hỗ trợ kiểm tra nội dung có tính ngữ nghĩa.
3. Metric: Mục tiêu là giảm thời gian rà soát từ 15–35 phút xuống dưới 5 phút và giảm số bài sai quy cách từ 6/30 xuống tối đa 1/30 bài.
4. Boundary: Công cụ chỉ đọc và cảnh báo lỗi, không tự ý chỉnh sửa file, commit, push hoặc nộp bài thay sinh viên.
5. Mức can thiệp AI: Nhóm lựa chọn Workflow bán tự động, sử dụng Rule-based làm chính và LLM cho một bước kiểm tra ngữ nghĩa hẹp.
6. Quyết định: Nhóm chọn GO để triển khai pilot ở phạm vi nhỏ, đồng thời đặt ra các điều kiện dừng nếu hệ thống hoạt động không hiệu quả.

---

## 7. Tài liệu tham khảo

- Tài liệu lab: [README.md](../../README.md), [CHECKPOINTS.md](../../CHECKPOINTS.md), [RUBRIC.md](../../RUBRIC.md), [SUBMISSION.md](../../SUBMISSION.md), [worksheet CP1–CP7](../../docs/01-worksheet.md), [bài deliverable mẫu](../../docs/02-deliverable-example.md), [các framework quốc tế](../../docs/03-international-frameworks.md).
- Báo cáo research và kiểm chứng của nhóm: [group_report.md](../team/group_report.md), [kịch bản phỏng vấn CP4](../assets/cp4-interview-script.md), [nhật ký eval CP6](../assets/cp6-eval-run.md).
- pre-commit, tài liệu chính thức: https://pre-commit.com/
- GitHub Classroom, tài liệu Autograding: https://docs.github.com/en/education/manage-coursework-with-github-classroom/teach-with-github-classroom/use-autograding
- Gradescope Autograder: https://www.gradescope.com/
- markdownlint-cli: https://github.com/igorshubovych/markdownlint-cli
