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
| Pitch Problem Card | | |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: | |
| Nhận phản biện | Câu hỏi tôi nhận được: | Tôi đã sửa gì: |
| Gom cluster / cây OST | | |
| Chọn candidate problem | | |
| Kiểm chứng / research | | |
| Quy trình nhóm | | |
| Problem Statement | | |
| Mức can thiệp AI | | |
| Quyết định | | |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | | | | |
| CP2 Problem Card | | | | |
| CP4 Research | | | | |
| CP5 Quy trình | | | | |
| CP5–6 Problem Statement | | | | |
| CP6 Mức can thiệp / quyết định | | | | |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

---

## 7. Tài liệu tham khảo

-
