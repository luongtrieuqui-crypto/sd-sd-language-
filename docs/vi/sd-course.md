# Lộ trình học Sd bằng tiếng Việt

Tài liệu này dành cho người mới bắt đầu và có thể dùng lâu dài làm giáo trình thực hành. Mỗi bài giải thích mục tiêu, đọc mã, bài tập và tiêu chí tự kiểm tra. Ví dụ dùng cú pháp Sd của IDE trong repository; không áp dụng cú pháp C/C++.

## Chuẩn bị

1. Mở `Sd IDE.html` bằng trình duyệt.
2. Chọn **Mở tệp** và mở một tệp trong `examples/sd/`.
3. Chọn **Chạy** để xem kết quả. Khi gặp lỗi, xem tab **Vấn đề** và đối chiếu số dòng.
4. Tạo một bản sao của bài trước khi thử nghiệm để có thể so sánh với bản gốc.

Mỗi lệnh trong các ví dụ Sd kết thúc bằng `ed`. Chương trình bắt đầu bằng `sta(main){` và khối chính đóng bằng `}`. Mẫu nhập thư viện I/O `imp*ioprt.ed` có trong ví dụ hiện tại.

## Bài 1 — Chương trình đầu tiên

Mở [`01_hello_world.sd`](../../examples/sd/01_hello_world.sd). Chương trình in một dòng chữ. Thử thay chuỗi trong dấu ngoặc kép rồi chạy lại.

Bạn cần nhận ra ba phần: dòng import, phần bắt đầu `main`, và lệnh `pri` dùng để in. Chuỗi phải đặt trong dấu ngoặc kép.

**Thực hành:** in tên của bạn và một câu giới thiệu trên hai dòng lệnh `pri` riêng.

**Tự kiểm tra:** sửa nội dung chuỗi có làm đổi kết quả không? Lệnh nào kết thúc bằng `ed`?

## Bài 2 — Biến số nguyên

Mở [`02_basic_math.sd`](../../examples/sd/02_basic_math.sd). Các biến `a`, `b`, `tong` lưu các số nguyên. Khai báo có dạng `iid: sta(int tên) => edt: sta(tên = biểu_thức) ed`. Sau khi khai báo, có thể dùng tên biến trong biểu thức và lệnh in.

Ví dụ ngắn:

```text
iid: sta(int a) => edt: sta(a = 12) ed
iid: sta(int b) => edt: sta(b = 8) ed
iid: sta(int tong) => edt: sta(tong = a + b) ed
iid: sta(pri) tong ed
```

Các phép toán số học cơ bản trong IDE gồm `+`, `-`, `*`, `/`, `%`. Dùng ngoặc để làm rõ thứ tự tính. Khi chia hai số nguyên, kết quả chia nguyên theo bộ thông dịch.

**Bài tập:** tính hiệu, tích và phần dư của `a` và `b`; đặt mỗi kết quả vào biến riêng, sau đó in nhãn và giá trị.

**Tự kiểm tra:** biến đã được khai báo trước khi sử dụng chưa? Tên biến có viết giống nhau ở mọi chỗ không?

## Bài 3 — Đọc trình tự thực thi

Bộ thông dịch chạy các lệnh trong khối `main` theo thứ tự từ trên xuống. Vì thế, hãy khai báo giá trị đầu vào trước, tính toán tiếp theo rồi mới in kết quả. Khi một phép tính phụ thuộc vào biến khác, biến đó phải được tạo trước.

**Bài tập mở rộng:** tạo chương trình tính tiền mua hàng với `so_luong`, `don_gia`, `tam_tinh`, `phi` và `tong_tien`. Dùng phép nhân để tính tạm tính, phép cộng để tính tổng. In từng thành phần để người dùng kiểm tra được kết quả.

Chia chương trình thành ba đoạn khi viết: khai báo dữ liệu, tính toán, trình bày kết quả. Dù chương trình ngắn, cách chia này giúp sửa dễ hơn khi thêm thuế hoặc giảm giá.

## Bài 4 — Chuỗi và đầu ra dễ đọc

Lệnh `pri` có thể in chuỗi đặt trong dấu ngoặc kép hoặc in một biểu thức/biến. Nên in nhãn riêng rồi in giá trị ở dòng kế tiếp nếu chưa dùng định dạng chuỗi.

Ví dụ:

```text
iid: sta(pri) "Tong tien:" ed
iid: sta(pri) tong_tien ed
```

**Bài tập:** chỉnh bài tính tiền để in các nhãn rõ nghĩa: số lượng, đơn giá, tạm tính, phí và tổng cộng. Chạy chương trình sau mỗi vài thay đổi thay vì sửa toàn bộ rồi mới chạy.

## Bài 5 — Lỗi thường gặp và cách tìm nguyên nhân

- **Thiếu `ed`:** kiểm tra cuối mỗi lệnh `iid:`.
- **Sai tên biến:** so sánh chính xác chữ hoa/chữ thường và cách viết tên ở chỗ khai báo với chỗ sử dụng.
- **Biến chưa khai báo:** thêm lệnh khai báo trước phép tính đầu tiên dùng biến đó.
- **Lỗi chia cho 0:** kiểm tra mẫu số trước khi chạy phép chia.
- **Sai cấu trúc chương trình:** kiểm tra `sta(main){` và dấu `}` đóng khối.
- **Không thấy đầu ra:** chắc chắn đã mở đúng tệp và bấm **Chạy**; xem tab **Vấn đề**.

IDE có thể gỡ lỗi từng bước và hiển thị biến. Đặt điểm dừng bằng cách bấm số dòng, chọn **Gỡ lỗi**, rồi quan sát biến sau từng bước.

## Bài tập tổng hợp — Báo cáo hình chữ nhật

Tạo tệp `examples/sd/04_rectangle_report.sd`:

1. Khai báo chiều dài và chiều rộng với giá trị dương.
2. Tính chu vi theo công thức `2 * (dài + rộng)`.
3. Tính diện tích theo công thức `dài * rộng`.
4. In tên báo cáo, hai kích thước, chu vi và diện tích.
5. Thử hai bộ kích thước khác nhau và xác nhận kết quả bằng phép tính tay.

## Lộ trình tiếp theo

Sau khi nắm biến, biểu thức và đầu ra, học điều kiện, vòng lặp, hàm và cấu trúc dữ liệu từ tài liệu tham khảo trong thư mục gốc. Cú pháp của các phần nâng cao cần được xác nhận bằng đặc tả và IDE; không suy luận rằng chúng giống ngôn ngữ khác. Xem [`docs/README.md`](../README.md) để tìm mục lục tài liệu và [`CODE_GUIDE.md`](../../CODE_GUIDE.md) để tìm hiểu IDE.
