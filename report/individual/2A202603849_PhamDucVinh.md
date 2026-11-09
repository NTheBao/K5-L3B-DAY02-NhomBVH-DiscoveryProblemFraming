# Báo cáo cá nhân — 2A202603849_PhamDucVinh

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Phạm Đức Vinh
- MSSV: 2A202603849
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: BVH
- Link repo nhóm: https://github.com/NTheBao/K5-L3B-DAY02-NhomBVH-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

|   # | Lăng kính                         | Job Story: Khi… tôi muốn… để…                                                                                                                                                                                  | Ai chịu ảnh hưởng?          | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng)                                                                                                                                                               |
| --: | --------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|   1 | Lặp lại                           | Khi tới kỳ kê khai, tôi muốn tải đủ hóa đơn mua vào và bán ra của tháng từ cổng hoadondientu.gdt.gov.vn về máy, để có bộ chứng từ đầy đủ trước khi lập tờ khai                                                 | Kế toán                     | ~450 hóa đơn/tháng trên 6 MST (150 mua vào + 300 bán ra); mỗi MST đăng nhập cổng riêng có captcha, tải file XML từng hóa đơn, ~20 giây/hóa đơn → ~2,5 giờ/tháng riêng bước tải, cả quy trình ~3 giờ; ~15 lần đăng nhập/tháng do 6 MST và hết phiên giữa chừng |
|   2 | Tốn thời gian                     | Khi đã tải danh sách hóa đơn từ cổng hoadondientu.gdt.gov.vn, tôi muốn đối chiếu với số liệu đã nhập trong phần mềm kế toán, để biết hóa đơn nào chưa hạch toán hoặc hạch toán sai số tiền                     | Kế toán                     | ~105 phút/tháng dò file Excel xuất từ cổng với sổ sách bằng mắt, lặp lại cho 6 MST; quý trước phát hiện 6 hóa đơn mua vào chưa hạch toán sau khi đã nộp tờ khai quý                                                                         |
|   3 | Cần đọc, tổng hợp nhiều thông tin | Khi lấy hóa đơn mua vào từ cổng, tôi muốn biết hóa đơn còn hợp lệ không (trạng thái hóa đơn trên cổng: bị thay thế, điều chỉnh hay hủy; người bán còn hoạt động theo MST), để không bị loại thuế được khấu trừ | Kế toán, giám đốc           | Phải xem trạng thái trên cổng hóa đơn rồi tra MST người bán ở trang tra cứu riêng, ~3 phút/hóa đơn; năm trước bị loại 2 hóa đơn khi quyết toán                                                                          |
|   4 | Tốn thời gian                     | Khi lập tờ khai thuế GTGT, tôi muốn tách đúng hóa đơn theo từng mức thuế suất, để số thuế trên tờ khai khớp với sổ sách                                                                                        | Kế toán                     | ~3 giờ/quý phân loại; 2/4 quý gần nhất phải nộp tờ khai bổ sung vì nhầm thuế suất                                                                                                                                       |
|   5 | Cần đọc, tổng hợp nhiều thông tin | Khi có hóa đơn đầu vào từ 20 triệu trở lên, tôi muốn biết khoản đó đã thanh toán bằng chuyển khoản chưa, để đủ điều kiện khấu trừ thuế                                                                         | Kế toán                     | ~15 hóa đơn/tháng phải dò sao kê ngân hàng, ~4 phút/hóa đơn                                                                                                                                                             |
|   6 | Pain từ người khác                | Khi nhân viên bán hàng xuất hóa đơn sai tên, MST hoặc số tiền, họ muốn biết cách điều chỉnh, để không phải nhờ kế toán làm lại từ đầu                                                                          | Nhân viên bán hàng, kế toán | ~8 hóa đơn sai/tháng; mỗi lần mất ~20 phút lập hóa đơn điều chỉnh hoặc thay thế                                                                                                                                         |
|   7 | Pain từ người khác                | Khi gần hạn nộp tờ khai quý, giám đốc muốn biết ước tính số thuế GTGT phải nộp, để chuẩn bị dòng tiền                                                                                                          | Giám đốc, kế toán           | Giám đốc hỏi ~10 lần/quý (đếm tin nhắn Zalo); mỗi lần kế toán mất ~30 phút tính tạm; 2/4 quý gần nhất số ước tính lệch hơn 10% so với số nộp thật                                                                       |
|   8 | Pain từ người khác                | Khi nhà cung cấp xuất hóa đơn sai tên công ty, sai MST hoặc xuất trễ tháng, tôi muốn biết sớm để yêu cầu họ sửa, để hóa đơn kịp kê khai đúng kỳ                                                                | Kế toán, nhà cung cấp       | ~5 hóa đơn/tháng phải yêu cầu sửa; trung bình 2 email/cuộc gọi nhắc mỗi hóa đơn, chờ 3–5 ngày nhà cung cấp phản hồi                                                                                                     |
|   9 | Lặp lại                           | Khi hóa đơn mua vào có ngày lập ở quý trước nhưng quý này mới xuất hiện trên cổng hoadondientu.gdt.gov.vn, tôi muốn biết nên đưa vào kỳ nào, để không kê khai sai kỳ                                           | Kế toán                     | ~6 hóa đơn "lệch kỳ"/quý; 1/4 quý gần nhất phải khai bổ sung vì lý do này                                                                                                                                               |
|  10 | Cần đọc, tổng hợp nhiều thông tin | Khi có văn bản mới về thuế suất hoặc hóa đơn (ví dụ giảm thuế GTGT), tôi muốn biết thay đổi nào áp dụng cho mặt hàng của công ty và từ ngày nào, để xuất hóa đơn và kê khai đúng                               | Kế toán, nhân viên bán hàng | ~3 văn bản/quý phải đọc, ~1 giờ/văn bản; đợt đổi thuế suất gần nhất có 12 hóa đơn bán ra xuất sai thuế suất phải điều chỉnh                                                                                             |

> **Bối cảnh:** kế toán dịch vụ làm kê khai thuế cho **nhiều công ty, mỗi công ty một MST riêng** (hiện ~6 MST, đều là công ty thương mại nhỏ). Tổng cộng ~150 hóa đơn đầu vào và ~300 hóa đơn đầu ra mỗi tháng trên cả 6 MST (trung bình ~25 mua vào + ~50 bán ra mỗi MST). Các công ty kê khai thuế GTGT **theo quý**. Với từng MST, kế toán phải đăng nhập cổng riêng và làm việc trên bộ sổ riêng trong phần mềm kế toán. Hạn nộp theo Luật Quản lý thuế là ngày cuối cùng của tháng đầu quý sau (quý 3 → 31/10); kế toán đặt mốc nội bộ nộp **cho tất cả MST** trước **ngày 28 của tháng đầu quý sau** (ví dụ 28/10 cho quý 3). Hóa đơn vẫn được lấy và đối chiếu hằng tháng để cuối quý không dồn việc. Nguồn lấy hóa đơn chính là cổng hóa đơn điện tử của Tổng cục Thuế (https://hoadondientu.gdt.gov.vn/): tra cứu theo tháng, xuất danh sách Excel và tải file hóa đơn về. Số liệu là giả định minh họa (số MST = 6 cần chỉnh theo thực tế).
>
> Dòng #1–#6 là tự scan, chưa dùng AI. Dòng #7–#10 là ý AI gợi ý, đã lọc và tự điền số liệu (xem ghi chú bên dưới).

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

- Tự scan trước được 6 ý (#1–#6). Dùng prompt CP1 trong worksheet (vai trò kế toán, nguồn hóa đơn là cổng hoadondientu.gdt.gov.vn, kèm 6 ý đã có) để hỏi AI thêm góc nhìn. AI gợi ý 8 ý; giữ lại 4 ý và tự điền số liệu của công ty:
  - #7 (giám đốc hỏi số thuế ước tính) và #8 (nhà cung cấp xuất hóa đơn sai/trễ): lăng kính "pain từ người khác" đang thiếu, có tin nhắn Zalo và email để đếm.
  - #9 (hóa đơn lệch kỳ trên cổng): gắn trực tiếp với việc lấy hóa đơn từ cổng, có số lần khai bổ sung.
  - #10 (theo dõi thay đổi quy định thuế): đúng lăng kính "cần đọc, tổng hợp", có số hóa đơn xuất sai sau đợt đổi thuế suất.
- Chưa đưa vào bảng: "khách hàng hỏi gửi lại hóa đơn" (ít liên quan tờ khai), "cơ quan thuế yêu cầu giải trình" (ít xảy ra, khó có baseline hằng tháng), "hóa đơn bán ra chênh lệch giữa cổng và sổ" (trùng với #2), "đọc từng dòng hàng để định khoản" (thuộc hạch toán, xa bài toán hóa đơn – tờ khai).
- Bỏ ý AI tự loại "tự động hóa toàn bộ quy trình kế toán" vì là giải pháp và quá rộng; bỏ "dự báo rủi ro bị thanh tra thuế" vì không có quy trình hằng tháng và khó đo.

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem                                               | Vì sao chọn                                                                                   | Điều còn chưa chắc                                                                   |
| ---: | ----------------------------------------------------- | --------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
|    1 | Đối chiếu hóa đơn trên cổng với phần mềm kế toán (#2) | Sót hóa đơn phải khai bổ sung, nhân lên theo số MST; quy trình rõ, bottleneck là một bước dò cụ thể | Hóa đơn bị sót vì dò sót, vì người bán đẩy lên cổng muộn, hay vì nhập liệu sót từ đầu? |
|    2 | Tải hóa đơn mua vào/bán ra từ cổng hoadondientu (#1)  | Tốn nhiều thời gian nhất (~3 giờ/tháng), lặp lại mỗi tháng, là đầu vào của card #1            | Cổng hoặc phần mềm kế toán đang dùng đã có sẵn cách lấy hóa đơn hàng loạt chưa?      |
|    3 | Kiểm tra hóa đơn mua vào còn hợp lệ (#3)              | Thiệt hại khi bị loại thuế khấu trừ, hiện chỉ kiểm được một phần hóa đơn                      | Bao nhiêu % nhà cung cấp lặp lại hằng tháng (nếu cao thì không cần tra lại mỗi lần)? |

### Problem Card #1

| Trường                                    | Nội dung                                                                                                                                                                                                                                                                               |
| ----------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Job Story                                 | Khi đã tải danh sách hóa đơn từ cổng hoadondientu.gdt.gov.vn, tôi muốn đối chiếu với số liệu đã nhập trong phần mềm kế toán, để biết hóa đơn nào chưa hạch toán hoặc hạch toán sai số tiền                                                                                             |
| Actor                                     | Kế toán dịch vụ phụ trách kê khai cho ~6 MST (6 công ty nhỏ), tự nhập hóa đơn vào phần mềm và tự đối chiếu cho từng MST                                                                                                                                                                                                                                      |
| Thời điểm / bối cảnh                      | Ngày 10–15 hằng tháng đối chiếu cho tháng trước, và đối chiếu lại toàn quý trước mốc nộp nội bộ ngày 28 của tháng đầu quý sau (ví dụ 28/10 cho quý 3); cả 6 MST dồn về cùng một mốc; ~25 hóa đơn mua vào + ~50 bán ra mỗi MST mỗi tháng                                                                    |
| Quy trình hiện tại (3–7 bước)             | Lặp lại cho từng MST: 1. Mở file Excel danh sách hóa đơn xuất từ cổng của MST đó · 2. Mở đúng bộ sổ của MST trong phần mềm kế toán, xuất sổ chi tiết hóa đơn · 3. Dò từng dòng hóa đơn mua vào theo số hóa đơn + MST người bán, so số tiền (hóa đơn bán ra chỉ so tổng) · 4. Đánh dấu hóa đơn thiếu/sai, hạch toán bổ sung · 5. Báo nhà cung cấp hoặc nhân viên liên quan về hóa đơn có vấn đề |
| Bottleneck (bước nào, mất bao nhiêu phút) | **Bước 3, dò từng dòng hóa đơn mua vào giữa 2 file bằng mắt: ~10 phút/MST × 6 = 60 phút/tháng** (~150 dòng, ~25 giây/dòng); hai file sắp xếp khác nhau, ký hiệu hóa đơn ghi khác định dạng, chuyển qua lại giữa các MST nên dễ nhầm và sót                                                                                                                                                |
| Impact (nếu không giải thì sao)           | ~105 phút/tháng ≈ 21 giờ/năm. Theo các tờ khai bổ sung 4 quý gần nhất trên 6 MST: 3/4 quý có hóa đơn mua vào bị sót, tổng 14 hóa đơn, ~18 triệu thuế GTGT đầu vào bị **khấu trừ chậm** (kê khai bổ sung ở kỳ sau, không mất hẳn); mỗi lần khai bổ sung mất thêm ~2 giờ và làm khách hàng mất tin tưởng                                                                 |
| Success metric (baseline → target)        | (1) Thời gian đối chiếu: ~105 → dưới 25 phút/tháng cho 6 MST, đo bằng bấm giờ. (2) Số hóa đơn sót phát hiện sau khi đã nộp tờ khai: 14 hóa đơn/4 quý → dưới 3 hóa đơn/4 quý, đo bằng số tờ khai bổ sung có lý do "sót hóa đơn"                                                                                        |
| Phương án không dùng AI                   | Ghép khóa "MST người bán + ký hiệu + số hóa đơn" ở cả 2 file, dùng XLOOKUP hoặc Power Query so khớp, tô màu dòng thiếu/lệch tiền bằng Conditional Formatting                                                                                                                           |
| Giả thuyết về AI (nếu có)                 | Có lẽ không cần: dữ liệu có cấu trúc, so khớp theo khóa là quy tắc cố định; lệch số tiền do làm tròn xử lý bằng ngưỡng dung sai                                                                                                                                                        |
| Cảm nhận nhanh                            | **Rule**                                                                                                                                                                                                                                                                               |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — ~105 phút/tháng cho 6 MST

[1 Mở Excel từ cổng: 1' × 6 = 6'] → [2 Mở đúng bộ sổ + xuất sổ: 2' × 6 = 12']
→ [3 Dò từng dòng hóa đơn mua vào: 10' × 6 = 60'] ← BOTTLENECK
→ [4 Đánh dấu + hạch toán bổ sung: 15'] → [5 Báo khách hàng / nhà cung cấp: 12']
```

### Problem Card #2

| Trường                                    | Nội dung                                                                                                                                                                                                                                         |
| ----------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Job Story                                 | Khi tới kỳ kê khai, tôi muốn tải đủ hóa đơn mua vào và bán ra của tháng từ cổng hoadondientu.gdt.gov.vn về máy, để có bộ chứng từ đầy đủ trước khi lập tờ khai                                                                                   |
| Actor                                     | Kế toán dịch vụ phụ trách ~6 MST                                                                                                                                                                                                                 |
| Thời điểm / bối cảnh                      | Đầu tháng (ngày 3–7) cho tháng trước; ~450 hóa đơn/tháng trên 6 MST                                                                                                                                                                                         |
| Quy trình hiện tại (3–7 bước)             | 1. Đăng nhập cổng bằng tài khoản của từng MST (MST, mật khẩu, captcha), tính cả lần đăng nhập lại do hết phiên · 2. Tra cứu theo tháng, xuất Excel danh sách mua vào và bán ra · 3. Tải file XML từng hóa đơn · 4. Đổi tên, xếp file vào thư mục theo tháng/nhà cung cấp |
| Bottleneck (bước nào, mất bao nhiêu phút) | **Bước 3, tải XML từng hóa đơn: ~20 giây × 450 hóa đơn ≈ 150 phút/tháng**; hết phiên giữa chừng phải đăng nhập lại và tìm lại vị trí đang tải                                                                                                    |
| Impact (nếu không giải thì sao)           | ~3 giờ/tháng ≈ 38 giờ/năm; phải giữ và chuyển qua lại 6 bộ tài khoản; việc tải dồn đầu tháng làm các bước sau (đối chiếu, lập tờ khai) bị đẩy sát hạn nộp; tải sót file dẫn tới thiếu chứng từ khi đối chiếu ở card #1                                                                      |
| Success metric (baseline → target)        | (1) Thời gian lấy đủ hóa đơn: ~190 → dưới 30 phút/tháng, đo bằng bấm giờ. (2) Số hóa đơn có trong danh sách Excel nhưng thiếu file XML khi đối chiếu: đo baseline 1 tháng → 0, đo bằng đếm dòng không có file tương ứng                          |
| Phương án không dùng AI                   | Kiểm tra cổng và phần mềm kế toán đang dùng có chức năng lấy hóa đơn hàng loạt từ cơ quan thuế không (cần tự kiểm); nếu không, chia việc tải thành mỗi tuần một lần thay vì dồn đầu tháng. Người vẫn tự đăng nhập và nhập captcha                |
| Giả thuyết về AI (nếu có)                 | Không cần AI: đây là thao tác lặp cố định, không cần hiểu nội dung                                                                                                                                                                               |
| Cảm nhận nhanh                            | **No AI** (dùng tính năng/công cụ có sẵn)                                                                                                                                                                                                        |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — ~190 phút/tháng cho 6 MST

[1 Đăng nhập từng MST + đăng nhập lại khi hết phiên: ~15 lần × 1' = 15'] → [2 Tra cứu + xuất Excel: 1,5' × 6 = 9']
→ [3 Tải XML từng hóa đơn: 150'] ← BOTTLENECK
→ [4 Đổi tên + xếp thư mục: 15']
```

### Problem Card #3

| Trường                                    | Nội dung                                                                                                                                                                                                                                                                                                                                   |
| ----------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Job Story                                 | Khi lấy hóa đơn mua vào từ cổng, tôi muốn biết hóa đơn còn hợp lệ không (trạng thái hóa đơn trên cổng, người bán còn hoạt động theo MST), để không bị loại thuế được khấu trừ                                                                                                                                                              |
| Actor                                     | Kế toán dịch vụ phụ trách ~6 MST; người chịu hậu quả cuối cùng là giám đốc các công ty khách hàng                                                                                                                                                                                                                                                                           |
| Thời điểm / bối cảnh                      | Khi nhận hóa đơn mua vào trong tháng; ~150 hóa đơn mua vào/tháng trên 6 MST nhưng chỉ kịp kiểm ~40 hóa đơn giá trị lớn hoặc của nhà cung cấp mới                                                                                                                                                                                                      |
| Quy trình hiện tại (3–7 bước)             | 1. Lọc hóa đơn cần kiểm (giá trị lớn, nhà cung cấp mới) · 2. Xem trạng thái hóa đơn trên cổng (hợp lệ, bị thay thế, điều chỉnh, hủy) · 3. Sang trang tra cứu riêng, nhập MST người bán để xem còn hoạt động · 4. Đọc lại tên, MST công ty mình, thuế suất, tổng tiền trên hóa đơn · 5. Ghi chú hóa đơn có vấn đề, yêu cầu nhà cung cấp sửa |
| Bottleneck (bước nào, mất bao nhiêu phút) | **Bước 3, tra MST người bán ở trang tra cứu riêng: ~1,5 phút/hóa đơn** (nhập MST, captcha, đọc kết quả); chiếm một nửa thời gian kiểm mỗi hóa đơn (~3 phút)                                                                                                                                                                                |
| Impact (nếu không giải thì sao)           | ~110 hóa đơn/tháng không được kiểm; năm trước bị loại 2 hóa đơn khi quyết toán, ~7 triệu thuế GTGT đầu vào không được khấu trừ                                                                                                                                                                                                             |
| Success metric (baseline → target)        | (1) Tỉ lệ hóa đơn mua vào được kiểm: 40/150 (27%) → 150/150 (100%), đo bằng số hóa đơn có ghi chú "đã kiểm". (2) Số hóa đơn bị loại khi quyết toán: 2/năm → 0                                                                                                                                                                              |
| Phương án không dùng AI                   | Lập danh sách nhà cung cấp đã kiểm kèm ngày tra MST, mỗi tháng chỉ tra lại nhà cung cấp mới hoặc đã lâu chưa tra; checklist 4 điểm cho bước 4                                                                                                                                                                                              |
| Giả thuyết về AI (nếu có)                 | Phần lớn là kiểm theo quy tắc (trạng thái, MST, thông tin bắt buộc). AI chỉ có thể hữu ích nếu cần đọc tên hàng hóa để phát hiện hàng không liên quan hoạt động kinh doanh; kế toán vẫn quyết định                                                                                                                                         |
| Cảm nhận nhanh                            | **Rule** (có thể Workflow nếu cần đọc tên hàng)                                                                                                                                                                                                                                                                                            |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — ~140 phút/tháng cho ~40 hóa đơn (3 phút/hóa đơn ở bước 2–4)

[1 Lọc hóa đơn cần kiểm: 10'] → [2 Xem trạng thái trên cổng: 0,5' × 40 = 20']
→ [3 Tra MST người bán ở trang riêng: 1,5' × 40 = 60'] ← BOTTLENECK
→ [4 Đọc thông tin hóa đơn: 1' × 40 = 40'] → [5 Ghi chú + yêu cầu sửa: 10']
```

### Card muốn pitch nhất

- Card số: 1 (Đối chiếu hóa đơn trên cổng với phần mềm kế toán)
- Vì sao: có bằng chứng từ tờ khai bổ sung, bottleneck là một bước dò cụ thể, khối lượng nhân lên theo số MST; câu hỏi chính cần kiểm chứng là Rule hoặc tính năng có sẵn trong phần mềm kế toán đã đủ chưa.
- Câu hỏi muốn nhóm phản biện: "Card #2 (tải hóa đơn) là đầu vào của card #1. Nên gộp thành một bài 'lấy và đối chiếu hóa đơn từ cổng', hay tách ra? Và nếu XLOOKUP là đủ, bài này còn đáng để nhóm đào sâu không?"

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra                                                                                      | Đồng ý?      | Đã sửa gì                                                                                                                   |
| ------------------------------------------------------------------------------------------------------- | ------------ | --------------------------------------------------------------------------------------------------------------------------- |
| Actor chưa đủ cụ thể: kế toán có tự nhập liệu không, hay chỉ đối chiếu? | Đồng ý một phần | Làm rõ actor là kế toán dịch vụ phụ trách ~6 MST, vừa nhập liệu vừa đối chiếu; sót đến từ khối lượng và việc 6 MST dồn về cùng mốc ngày 28 |
| 60 phút dò ~450 dòng (~8 giây/dòng) là quy trình tưởng tượng | Đồng ý | Làm rõ chỉ dò từng dòng hóa đơn mua vào (~150 dòng, ~25 giây/dòng), hóa đơn bán ra chỉ so tổng; tính lại quy trình thành ~105 phút cho 6 MST |
| Bottleneck có thể sai chỗ: hóa đơn sót vì người bán đẩy lên cổng muộn hoặc nhập liệu sót từ đầu | Đồng ý | Ghi vào "Điều còn chưa chắc" của card #1 để kiểm chứng ở CP4 (phân loại 14 hóa đơn sót theo nguyên nhân) |
| 18 triệu là khấu trừ chậm, không phải mất tiền; target "→ 0" tuyệt đối, không thực tế | Đồng ý | Sửa Impact thành "khấu trừ chậm"; đổi target thành dưới 3 hóa đơn/4 quý |
| Phần mềm kế toán có thể đã có sẵn tính năng lấy và đối chiếu hóa đơn với cơ quan thuế | Đồng ý | Đưa vào research CP4; nếu đã có, kết luận nghiêng về No AI (dùng tính năng có sẵn) |
| Card tự kết luận Rule nhưng lý do pitch lại nói "so sánh rõ 4 mức" | Không đồng ý một phần | Kết luận Rule vẫn hợp lệ nếu lập luận chặt; đã sửa lý do pitch thành "kiểm chứng Rule/tính năng có sẵn đã đủ chưa" |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động                  | Tôi đã làm gì?         | Kết quả / ảnh hưởng tới bài nhóm |
| -------------------------- | ---------------------- | -------------------------------- |
| Pitch Problem Card         | Pitch 3 card về hóa đơn điện tử cho kế toán dịch vụ: #4 đối chiếu hóa đơn cổng – phần mềm kế toán, #5 tải hóa đơn từ cổng, #6 kiểm tra hóa đơn hợp lệ | Card #4 được đưa vào shortlist, xếp thứ 2 (27/35), sau card #1 của Hiếu (31/35) |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: hỏi Hiếu (#1) "Con số 6 bạn bị trừ điểm ở Day 01 lấy từ đâu, có bảng điểm không?"; hỏi Hiếu (#2) "Pre-commit hook với Flake8/Black đã chặn được lỗi format, phần còn lại là gì?"; hỏi Bảo (#7) lần bỏ sót yêu cầu gần nhất và con số 2–3 lần/tuần có ghi chép không; hỏi Bảo (#9) chỉ dùng template bug report bắt buộc là đủ chưa | Câu hỏi cho #1 làm điểm Pain chỉ còn 4/5 và đưa con số "≥6 bạn" vào Assumption Map để kiểm chứng ở CP4 (TA xác nhận 6/30 bài); câu hỏi cho #2 và #9 góp phần loại hai card này vì Rule/No AI đã giải được phần lớn |
| Nhận phản biện             | Câu hỏi tôi nhận được: Hiếu hỏi "Số liệu 6 MST và 14 hóa đơn sót là thật hay giả định? Nếu XLOOKUP là đủ thì bài còn đáng đào sâu không?"; Bảo hỏi "Phần mềm kế toán đang dùng đã có chức năng lấy hóa đơn hàng loạt từ cơ quan thuế chưa?" | Tôi đã sửa gì: thừa nhận số liệu card #4 là giả định minh họa, chấm Pain 3/5 và Domain 2/5; ghi rõ card #5 có thể đã giải bằng tính năng có sẵn (No AI) |
| Gom cluster / cây OST      | Hỗ trợ cập nhật lại mục 2 (CP3) trong `group_report.md` (commit `cf3eab4` "update lại CP3") | Pitch, cluster, OST và bảng chấm điểm được chỉnh lại trước khi sang CP4 |
| Chọn candidate problem     | Ban đầu bảo vệ card #4 vì metric rõ hơn; sau khi nhóm đặt tiêu chí "kiểm chứng được trong buổi lab" và "nhóm hiểu domain" lên trước, tôi đồng ý chọn #1 | Nhóm chọn #1 "Rà soát quy cách bài nộp theo rubric"; lý do loại #4 được ghi lại ở mục 2.4 |
| Kiểm chứng / research      | Người chính phần kiểm chứng CP4: chấm lại Assumption Map, soạn kịch bản phỏng vấn The Mom Test (`report/assets/cp4-interview-script.md`); hỗ trợ research: tìm pre-commit, tự kiểm từng link trong bảng 3.3, bỏ claim không nguồn (commit `734e2bd` "update cp4") | Nhóm có 5 snapshot và bảng research có link đã kiểm; kết luận "Rule trước, AI sau" và boundary read-only lấy từ kết quả này |
| Quy trình nhóm             | Đối chiếu mục 4 với `SUBMISSION.md`, `RUBRIC.md`, `CHECKPOINTS.md`: bổ sung số bước và số bước thủ công vào bảng before/after, thời gian bước 6, phương án quay về khi Rule lỗi; bỏ bước "tự động commit, push" | Quy trình tương lai khớp boundary read-only; sơ đồ Mermaid được giữ ngay trong báo cáo theo đúng `SUBMISSION.md` |
| Problem Statement          | Phản biện Problem Statement v0: chỉ ra đang lẫn giải pháp, Impact "trừ 5–10%" không có nguồn, target "0%" không đo được | Impact được thay bằng quy định trong `RUBRIC.md`, target đổi thành ≤ 1/30 bài, v1 có thêm metric chất lượng |
| Mức can thiệp AI           | Hỗ trợ CP6: chạy bộ 10 test case cho bước LLM với một prompt cố định, thêm quy tắc cấm nhận xét ngoài phạm vi sau lần chạy nháp, ghi nhật ký `report/assets/cp6-eval-run.md` | Kết quả 10/10 đạt, 0 ca bịa tiêu chí; đây là bằng chứng để giữ mức Workflow có AI ở một bước hẹp |
| Quyết định                 | Hỗ trợ đánh giá 4 rủi ro; đề xuất ghi rủi ro Value ở mức Trung bình vì phần LLM chưa có bằng chứng từ CP4 | Quyết định Go phạm vi nhỏ; kết quả eval được dùng làm điều kiện bật bước LLM trong pilot (mục 8.2) |

---

## 5. Dùng AI

| Checkpoint                     | Tôi dùng AI để làm gì?                                                                                | AI hữu ích ở đâu?                                                                                                                                    | AI sai hoặc hời hợt ở đâu?                                                                                                                                                            | Tôi sửa gì bằng nhận định của mình?                                                                                                       |
| ------------------------------ | ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| CP1 Scan                       | Sau khi tự scan 6 ý, dùng prompt CP1 nhờ AI gợi ý thêm theo 4 lăng kính, ưu tiên "pain từ người khác" | Nhắc ra các bên liên quan chưa nghĩ tới: giám đốc cần số thuế ước tính, nhà cung cấp xuất sai/trễ, hóa đơn lệch kỳ trên cổng, thay đổi quy định thuế | Có ý trùng với ý đã có (chênh lệch cổng – sổ trùng #2), ý ít xảy ra khó đo (giải trình với cơ quan thuế), ý lệch khỏi bài toán (định khoản); cách đo AI đưa ra chưa có số của công ty | Chỉ giữ 4 ý đo được bằng dữ liệu của công ty, tự điền con số (số tin nhắn, số hóa đơn sửa, số lần khai bổ sung); bỏ ý trùng và ý quá rộng |
| CP2 Problem Card | Dùng prompt phản biện CP2, nhờ AI đóng vai "PM hoài nghi" phản biện card #1 (đối chiếu cổng – phần mềm kế toán) | Bắt được quy trình phi thực tế (8 giây/dòng), impact bị thổi phồng (khấu trừ chậm chứ không mất), bottleneck có thể nằm ở người bán hoặc khâu nhập liệu | Giả định kế toán chỉ làm cho 1 công ty; thực tế kế toán dịch vụ làm cho nhiều MST | Sửa actor thành kế toán phụ trách ~6 MST, tính lại quy trình và impact; đưa nguyên nhân sót và tính năng có sẵn của phần mềm vào kiểm chứng CP4 |
| CP4 Research | Dùng Claude Code chấm lại Assumption Map, soạn kịch bản phỏng vấn The Mom Test (`report/assets/cp4-interview-script.md`) và tìm công cụ đã giải bài tương tự (pre-commit, GitHub Classroom autograding, markdownlint, Gradescope) | Chỉ ra tín hiệu phản bác bị bỏ sót trong snapshot của TA (TA đã có script kiểm tên file); tìm ra pre-commit là công cụ sinh viên tự chạy được trước khi nộp | Bản research cũ có claim không nguồn ("Gradescope bản quyền đắt"); công cụ đọc web của AI lỗi nên phải tự kiểm link bằng lệnh `curl` | Tự kiểm từng link (đều mở được) trước khi đưa vào bảng 3.3; bỏ claim không nguồn; giữ kết luận "Rule trước" vì khớp với bằng chứng phỏng vấn |
| CP5 Quy trình | Nhờ AI đối chiếu mục 4 với `RULES.md`, `CHECKPOINTS.md`, worksheet, bài mẫu, `RUBRIC.md`, `SUBMISSION.md` và chỉ ra chỗ thiếu | Bắt được bảng before/after thiếu "số bước" và "số bước thủ công", thiếu thời gian bước 6, thiếu phương án quay về khi Rule lỗi | AI từng khẳng định sai rằng phải lưu sơ đồ Mermaid thành file trong `report/assets/`; `SUBMISSION.md` quy định viết thẳng khối `mermaid` trong báo cáo | Đọc lại `SUBMISSION.md` và giữ Mermaid trong báo cáo; tự quyết định bỏ bước "tự động commit, push" vì trái boundary read-only |
| CP5–6 Problem Statement | Nhờ AI đóng vai PM hoài nghi chỉ ra lỗ hổng của Problem Statement v0 (không viết lại thay) | Chỉ ra Problem Statement đang chứa giải pháp, Impact "trừ 5–10%" không nguồn, target "0%" không đo được, metric chỉ đo tốc độ | Lúc đầu AI chưa thấy `RUBRIC.md` đã có quy định trừ 5 điểm cho sai tên file | Thay Impact bằng quy định trong `RUBRIC.md`; đổi target thành ≤ 1/30 bài; thêm metric chất lượng ở v1 |
| CP6 Mức can thiệp / quyết định | Nhờ AI so sánh 4 mức và lập luận cho từng lựa chọn; nhờ AI chạy thật bộ 10 test case cho bước LLM bằng Claude Code CLI với một prompt cố định, chấm từng ca theo 5 tiêu chí nhóm (nhật ký: `report/assets/cp6-eval-run.md`) | Nêu rõ đánh đổi mức Rule/Workflow; chạy đủ 10 ca trong vài phút, mỗi cảnh báo đều trích nguyên văn yêu cầu từ `CHECKPOINTS.md`/`RUBRIC.md`/worksheet, kể ca khó nhất TC-05 (Job Story lẫn giải pháp mà không có từ khóa "AI") | Lần chạy nháp với prompt chưa có quy tắc giới hạn phạm vi, AI nhận xét thêm "viết chung chung" ở TC-10 và "mẫu 2 bài lab còn nhỏ" ở TC-02 — báo nhầm ngoài phạm vi, sẽ trượt tiêu chí 5 nếu tính; lần trước AI còn ghi "Đạt" cho 10 test case chưa chạy | Thêm quy tắc cấm nhận xét ngoài phạm vi vào prompt rồi chạy lại đủ 10 ca: 10/10 đạt, 0 ca trượt tiêu chí 2; tự đối chiếu từng căn cứ AI trích với nguyên văn trong file hướng dẫn trước khi ghi kết quả; tự chốt mức Workflow có AI ở một bước hẹp và ghi rủi ro Value là Trung bình |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

Cả 3 card của tôi đều xoay quanh hóa đơn điện tử, tôi viết khá kỹ quy trình và con số. Nhưng khi nghe Hiếu pitch card rà soát quy cách bài nộp, tôi nhận ra card tốt chưa chắc là card nên chọn: card của Hiếu có sự kiện thật (≥6 bạn bị trừ điểm ở Day 01) và cả nhóm đều là người dùng, nên kiểm chứng được ngay trong buổi lab. Card của Bảo về bug report thì cho tôi thấy nhiều bài toán đã có lời giải No AI (một template bắt buộc các trường) trước khi cần nghĩ tới AI.

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

Có. Khi vẽ cây OST, nhóm viết ra mấy nhánh như "bot Discord tự chạy script kiểm tra format", "LLM đọc rubric tự sinh checklist", "macro Excel/XLOOKUP so khớp hóa đơn". Đọc lại thì đó là công cụ, không phải nỗi đau. Nhóm gạch bỏ từng ý và viết lại thành opportunity, ví dụ "dò tay tên file khi mệt dễ sót ký tự". Problem Statement v0 cũng từng có câu mang giải pháp, phải tách ra khỏi phần mô tả vấn đề.

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

Có. Lúc chọn candidate tôi bảo vệ card #4 (đối chiếu hóa đơn) vì metric rõ hơn. Hiếu hỏi thẳng: "Số liệu 6 MST và 14 hóa đơn sót là thật hay giả định?". Tôi phải thừa nhận đó là số minh họa và nhóm không có kế toán thật nào để phỏng vấn trong buổi lab. Tôi chấp nhận chấm Pain 3/5, Domain 2/5 và đồng ý chọn #1. Ở CP6 tôi cũng đổi ý: ban đầu tin kết quả eval "Đạt" ghi sẵn, sau đó chạy thật mới thấy prompt nháp báo nhầm ở TC-02 và TC-10.

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

Bất ngờ nhất là trợ giảng đã có sẵn script Bash kiểm tên file khi chấm. Nghĩa là phần lớn bài toán đã giải được bằng Rule, chỉ là sinh viên không có script đó để tự chạy trước khi nộp. Điều thứ hai là người được hỏi không muốn công cụ tự sửa bài, chỉ muốn được chỉ ra dòng sai. Hai điều này khiến nhóm chốt boundary read-only và "Rule trước, AI sau".

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

Khó nhất là viết Impact và target có nguồn. Bản đầu ghi "trừ 5–10% điểm" và target "0% lỗi" nghe hợp lý nhưng không có căn cứ và không đo được. Phải quay lại `RUBRIC.md` để lấy mức trừ 5 điểm, lấy 6/30 bài từ lời TA làm baseline và đổi target thành ≤ 1/30. Giữ cho Problem Statement không chứa giải pháp cũng khó, vì nhóm đã nghĩ sẵn tới script và LLM.

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

Tôi sẽ đòi bằng chứng sớm hơn, ngay từ CP3, thay vì để tới CP4 mới phát hiện con số "sót lỗi 15%" không có nguồn. Tôi cũng sẽ phản biện mạnh hơn việc thêm bước LLM: bằng chứng phỏng vấn chủ yếu ủng hộ phần Rule, chưa ai kể bị trừ điểm vì Success Metric thiếu baseline. Vì vậy rủi ro Value của bước LLM chỉ là Trung bình, và lẽ ra nhóm nên thử pilot Rule thuần trước rồi mới tính tới LLM.

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi _problem → quy trình → metric → boundary → mức can thiệp AI → quyết định_ của bài nhóm mình.

Problem: sinh viên sát hạn 23h59 phải tự dò tên file, thư mục và các mục bắt buộc nên hay sai quy cách và bị trừ 5 điểm oan. Quy trình hiện tại có 6 bước, bottleneck là bước 2–3 dò bằng mắt mất khoảng 20 phút (phỏng vấn ghi nhận 15–35 phút). Metric: số bài sai quy cách từ 6/30 xuống ≤ 1/30 và thời gian rà soát xuống dưới 5 phút, kèm metric chất lượng là Rule không bỏ sót lỗi và LLM báo nhầm ≤ 2/10. Boundary: công cụ chỉ đọc và báo lỗi, không sửa file, không commit, push hay nộp bài; sinh viên tự kiểm tra cảnh báo và tự quyết định. Mức can thiệp: Workflow có AI ở một bước hẹp, Rule checker làm phần chính, LLM chỉ cảnh báo tùy chọn cho các mục cần đọc hiểu như Success Metric hay Job Story lẫn giải pháp. Không chọn Agent vì các bước đã cố định và quyền sửa, nộp thuộc về sinh viên. Quyết định: Go phạm vi nhỏ, pilot 2 bài lab; bước LLM chỉ bật khi đạt eval (đã chạy 10/10) và sẽ tắt nếu báo nhầm quá 2/10 hoặc bịa tiêu chí.

---

## 7. Tài liệu tham khảo

- Đề bài và hướng dẫn của lab: `README.md`, `CHECKPOINTS.md`, `RUBRIC.md`, `SUBMISSION.md`, [docs/01-worksheet.md](../../docs/01-worksheet.md), [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md), [docs/03-international-frameworks.md](../../docs/03-international-frameworks.md)
- Báo cáo nhóm: [report/team/group_report.md](../team/group_report.md); kịch bản phỏng vấn [report/assets/cp4-interview-script.md](../assets/cp4-interview-script.md); nhật ký eval [report/assets/cp6-eval-run.md](../assets/cp6-eval-run.md)
- Cổng hóa đơn điện tử của Tổng cục Thuế (bối cảnh card CP1–CP2): https://hoadondientu.gdt.gov.vn
- Rob Fitzpatrick, *The Mom Test*: https://www.momtestbook.com/
- Intercom, Job Stories: https://www.intercom.com/blog/accidentally-invented-job-stories/
- Teresa Torres, Opportunity Solution Trees: https://www.producttalk.org/opportunity-solution-trees/
- Anthropic, Building effective agents: https://www.anthropic.com/research/building-effective-agents
- Google PAIR, People + AI Guidebook (User Needs): https://pair.withgoogle.com/chapter/user-needs/
- pre-commit: https://pre-commit.com/
- GitHub Classroom, Use autograding: https://docs.github.com/en/education/manage-coursework-with-github-classroom/teach-with-github-classroom/use-autograding
