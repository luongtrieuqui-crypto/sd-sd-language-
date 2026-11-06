# Học Sd++ bằng tiếng Việt: Giáo trình thực hành

Tài liệu này đi từ cấu trúc tệp đến biến và biểu thức số, đồng thời hướng dẫn cách tự luyện tập và tìm lỗi. Ví dụ dùng cú pháp Sd++ mà IDE trong repository đang xử lý; Sd++ ở đây không phải C++.

## Chuẩn bị và quy tắc tệp

Mở `Sd IDE.html`, chọn **Mở tệp**, rồi tải một tệp `.sdpp` trong `examples/sdpp/`. Chọn **Chạy** để thực thi. Tệp Sd++ mẫu có khung `ssta { ... }`, khối `define [...]`, lệnh kết thúc bằng `$` và dấu kết thúc tệp `##`. Hãy giữ đủ các dấu này.

## Bài 1 — Khung chương trình và lệnh in

Mở [`01_hello_world.sdpp`](../../examples/sdpp/01_hello_world.sdpp). Đọc từ ngoài vào trong: `ssta {` mở phần Sd++, `define` chỉ định tên điểm bắt đầu, `main: {` mở thân chương trình, `ids.pri:` in dữ liệu, sau đó các dấu đóng khối và `##` kết thúc tệp.

**Thực hành:** đổi lời chào thành câu của riêng bạn. Thêm một lệnh `ids.pri:` để in thêm dòng thứ hai. Chạy lại sau mỗi thay đổi.

**Tự kiểm tra:** lệnh có kết thúc bằng `$` không? Tệp có `##` ở cuối không? Khối `main` đã được đóng chưa?

## Bài 2 — Biến và phép tính

Mở [`02_basic_math.sdpp`](../../examples/sdpp/02_basic_math.sdpp). Khai báo số nguyên và gán giá trị ban đầu theo dạng `iptedt.int tên = biểu_thức $`. Dùng tên biến trong biểu thức tiếp theo, rồi in bằng `ids.pri:`.

```text
iptedt.int a = 12 $
iptedt.int b = 8 $
iptedt.int tong = a + b $
ids.pri: "Tong hai so la:" $
ids.pri: tong $
```

Các phép toán cơ bản gồm `+`, `-`, `*`, `/`, `%`. Viết biểu thức thành nhiều biến trung gian nếu điều đó giúp kiểm tra được từng bước.

**Bài tập:** thêm biến `hieu`, `tich`, `thuong_nguyen`; tính lần lượt hiệu, tích và phép chia nguyên. In nhãn riêng cho mỗi kết quả. Không chia cho giá trị 0.

## Bài 3 — Tính toán có tổ chức

Một chương trình dễ bảo trì nên chia thành ba phần: khai báo dữ liệu, tính toán, và trình bày kết quả. Đặt tên biến có nghĩa, ví dụ `chieu_dai`, `chieu_rong`, `dien_tich`, thay vì tên khó nhớ. Khi biểu thức dài, dùng biến trung gian và đối chiếu kết quả bằng tính tay.

**Bài tập:** mở [`03_rectangle_area.sdpp`](../../examples/sdpp/03_rectangle_area.sdpp), thêm phép tính chu vi `2 * (chieu_dai + chieu_rong)` và in kết quả. Thử nhiều kích thước để kiểm tra.

## Bài 4 — Đọc lỗi và gỡ lỗi

- **Thiếu dấu `$`:** mọi lệnh Sd++ thông thường trong ví dụ cần dấu kết thúc.
- **Thiếu `##`:** đảm bảo dấu này còn ở cuối tệp.
- **Tên biến chưa khai báo:** khai báo trước khi dùng trong biểu thức.
- **Sai phép tính:** kiểm tra thứ tự tính và thử các giá trị nhỏ có thể tính tay.
- **Không thấy đầu ra:** kiểm tra đúng tệp đang mở, bấm **Chạy**, rồi xem tab **Vấn đề**.

Dùng **Gỡ lỗi** và điểm dừng trên số dòng để quan sát biến trong khi chạy. Sửa một lỗi mỗi lần, rồi chạy lại để xác định chính xác tác động của thay đổi.

## Bài tập tổng hợp — Kế hoạch chi tiêu

Tạo tệp `examples/sdpp/04_budget_report.sdpp` với các phần sau:

1. Khai báo `so_luong`, `don_gia`, `phi_van_chuyen`.
2. Tính `tam_tinh = so_luong * don_gia`.
3. Tính `tong_tien = tam_tinh + phi_van_chuyen`.
4. In từng giá trị cùng nhãn dễ hiểu.
5. Thử số lượng 1 và một số lượng lớn hơn; xác nhận kết quả bằng tính tay.

## Thêm bài học mới

Đặt chương trình trong `examples/sdpp/` với tên có số thứ tự và chủ đề, ví dụ `05_bieu_thuc.sdpp`. Mỗi tệp là chương trình độc lập. Cập nhật README của thư mục khi thêm bài. Tham khảo [mục lục tài liệu](../README.md) và [hướng dẫn mã nguồn tiếng Việt](../../CODE_GUIDE.md).

Các cấu trúc nâng cao như điều kiện, vòng lặp, hàm và bộ nhớ cần được học từ tài liệu đặc tả/giáo trình và xác nhận bằng IDE. Không tự suy ra rằng cú pháp của chúng giống C++.
