# Giải thích mã nguồn Sd / Sd++

Tài liệu này giải thích những phần mã nguồn có trong repository. Các ví dụ trong `sdform.sd` và `shortsd.sd` là mã Sd theo cú pháp riêng của dự án, **không phải cú pháp C/C++**. Một số file ví dụ được viết rất gọn trên một dòng nên phần giải thích bên dưới mô tả cấu trúc và ý nghĩa của các lệnh, không giả định rằng chúng đã được định dạng lại hay kiểm thử độc lập.

## 1. `Sd IDE.html` — IDE và bộ thông dịch trên trình duyệt

Đây là một ứng dụng HTML độc lập: phần `<style>` định nghĩa giao diện, phần `<div id="app">` tạo các vùng UI, còn phần `<script>` triển khai phân tích và chạy chương trình Sd.

### Giao diện

- Thanh công cụ cung cấp chạy, gỡ lỗi, chọn ví dụ/mẫu lệnh, định dạng, mở/lưu và sao chép tệp.
- Khu vực soạn thảo gồm số dòng, vùng mã và đánh dấu cú pháp/lỗi.
- Bảng bên cạnh chia thành các tab đầu ra, biến, nhập liệu, vấn đề và tra cứu.
- CSS dùng biến màu và media query để hỗ trợ giao diện sáng/tối, màn hình nhỏ và tùy chọn giảm chuyển động.

### Bộ xử lý ngôn ngữ

- `SdFault` mang mã lỗi, thông báo và số dòng để IDE có thể trình bày lỗi theo vị trí.
- `stripComments`, `tokenize`, lớp `P` và `parseExpr` lần lượt xử lý chú thích, tách token và phân tích biểu thức.
- `Prog` phân tích cấu trúc chương trình Sd như hàm, cấu trúc dữ liệu, lệnh điều kiện/vòng lặp và import.
- `PProg` mở rộng bộ phân tích cho Sd++, gồm tiền xử lý và các cấu trúc riêng của biến thể này.
- `VM` thực thi chương trình: quản lý biến và phạm vi, gọi hàm, tính biểu thức, nhập/xuất, con trỏ, heap và các giới hạn an toàn.
- Lớp IDE kết nối bộ phân tích/VM với trình soạn thảo, bảng điều khiển và debugger. Các điểm dừng và lệnh chạy từng bước giúp quan sát chương trình khi thực thi.

### Luồng chạy tổng quát

1. Người dùng nhập hoặc mở mã nguồn trong vùng soạn thảo.
2. IDE phân tích mã và hiển thị lỗi/cảnh báo nếu phát hiện vấn đề.
3. Khi chạy, chương trình được thực thi trong VM; dữ liệu nhập lấy từ tab Nhập liệu hoặc lời nhắc tương tác.
4. IDE đưa đầu ra, lỗi và thông tin biến/debug lên các tab tương ứng.

## 2. `sdform.sd` và `shortsd.sd` — ví dụ ngôn ngữ

Hai file này chứa ví dụ Sd. `shortsd.sd` trình bày nhiều cấu trúc trên một dòng; `sdform.sd` có chú thích trong mã giúp người đọc nhận biết mục đích của các phần. Khi đọc, hãy dùng dấu phân tách và từ khóa của Sd đúng như tài liệu ngôn ngữ, không thay chúng bằng cú pháp của ngôn ngữ khác.

Những thành phần thể hiện trong ví dụ gồm:

- `imp...` — lệnh nhập thư viện/tệp; ví dụ có nhắc đến thư viện I/O và toán học.
- Phần định nghĩa hàm `diem` và khối `main` — minh họa khai báo hàm và điểm bắt đầu chương trình.
- Khai báo biến kiểu `int`, `float`, `str` — minh họa dữ liệu có kiểu.
- Lệnh `ipt` — đọc dữ liệu vào biến; lệnh `pri` — in đầu ra.
- Các dạng `for`, `while` và khối điều kiện — minh họa điều khiển luồng.
- Khai báo cấu trúc và hàm `void` — minh họa cấu trúc dữ liệu và hàm không trả giá trị.

Ví dụ có thể chứa nhiều cấu trúc ghép lại nhằm minh họa cú pháp; đừng xem mỗi dòng là một bài tập độc lập hay giả định mọi đoạn đều là ví dụ chạy riêng. Để xác nhận một chương trình, hãy mở file trong `Sd IDE.html`, kiểm tra tab Vấn đề rồi chạy thử.

## 3. Tài liệu ngôn ngữ

Các file `.tex`, `.txt` và `.pdf` là tài liệu tham khảo/giáo trình của dự án. Nên dùng chúng để xác nhận chính xác cú pháp, dấu kết thúc lệnh, kiểu dữ liệu và khác biệt giữa Sd với Sd++ trước khi thay đổi ví dụ.

## 4. Giới hạn của phần giải thích

Hướng dẫn này giải thích cấu trúc và vai trò của mã ở mức có thể suy ra từ các file trong repository; đây không phải bản đặc tả đầy đủ của Sd/Sd++. Một số file là minified/viết gọn, và giao diện IDE cùng nhiều thông báo hiện đang bằng tiếng Việt.
