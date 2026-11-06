# Lộ trình học dài hạn Sd / Sd++

Tài liệu này là kế hoạch học tập từ cơ bản đến nâng cao, dùng để phát triển repo thành khóa học thực hành. Mỗi giai đoạn có mục tiêu, sản phẩm cần làm, và file mẫu liên quan.

## Mục tiêu

- Học cú pháp chính thức của Sd và Sd++ theo bộ thông dịch của repo.
- Duy trì nhiều ví dụ nhỏ nhưng có chủ đề rõ ràng.
- Biết cách so sánh, sửa, và mở rộng các ví dụ mà không phá cấu trúc repo.
- Dùng repo như một notebook học tập và tài liệu tham khảo cho người mới.

## Giai đoạn 1 — Làm quen với IDE

- Mục tiêu: mở file, chạy chương trình, đọc lỗi, gỡ lỗi từng bước.
- File cần đọc: `Sd IDE.html`, `README.md`, `README.vi.md`, `docs/README.md`.
- Kết quả mong muốn: người học biết cách mở tệp `.sd` và `.sdpp`, đọc tab Vấn đề, và chạy chương trình trên IDE.

## Giai đoạn 2 — Cơ bản về Sd

- Mục tiêu: hiểu cấu trúc, import, main, biến, phép toán, đầu ra.
- File mẫu: `examples/sd/01_hello_world.sd`, `02_basic_math.sd`.
- Bài tập: thêm 3 ví dụ mới: `03_input_output.sd`, `04_variable_math.sd`, `05_report.sd`.

## Giai đoạn 3 — Cơ bản về Sd++

- Mục tiêu: hiểu khung `ssta`, `define`, `main`, `ids.pri`, biến kiểu và ký hiệu `$`.
- File mẫu: `examples/sdpp/01_hello_world.sdpp`, `02_basic_math.sdpp`, `03_rectangle_area.sdpp`.
- Bài tập: thêm 3 ví dụ mới theo cùng cách: `04_output_format.sdpp`, `05_math_flow.sdpp`, `06_report.sdpp`.

## Giai đoạn 4 — Điều kiện và vòng lặp

- Mục tiêu: viết chương trình có nhánh và lặp.
- Nhiệm vụ: tạo mẫu trong `examples/sd/` và `examples/sdpp/` cho dạng `if/else`, `for`, `while`.
- Kết quả mong muốn: người học biết cách tách logic thành nhiều khối rõ ràng và dễ kiểm tra.

## Giai đoạn 5 — Hàm và mô-đun hóa

- Mục tiêu: chia logic thành nhiều hàm/khối và một chương trình có cấu trúc đọc được.
- File mẫu: dùng các ví dụ đã có làm nền; thêm `lesson_function.sd` và `lesson_function.sdpp`.
- Yêu cầu: mỗi hàm chỉ giải quyết 1 nhiệm vụ; tên biến rõ nghĩa; tên file mô tả chủ đề.

## Giai đoạn 6 — Mảng, cấu trúc dữ liệu và dữ liệu lớn hơn

- Mục tiêu: xử lý tập dữ liệu theo nhóm, cấu trúc dữ liệu đơn giản.
- Nhiệm vụ: tạo ví dụ về danh sách số, tập hợp dữ liệu đầu vào, báo cáo tổng hợp.
- Kết quả mong muốn: người học biết cách tách dữ liệu, xử lý và in kết quả một cách rõ ràng.

## Giai đoạn 7 — Tự làm dự án mini

- Dự án 1: máy tính đơn giản
- Dự án 2: tính toán hóa đơn
- Dự án 3: báo cáo số liệu
- Dự án 4: quản lý điểm số/quản lý sinh viên đơn giản

Mỗi dự án nên nằm trong một file riêng hoặc một thư mục con trong `examples/` để dễ chạy và so sánh.

## Quy tắc đặt tên khi thêm bài mới

- Sử dụng số thứ tự: `01_`, `02_`, `03_` ...
- Tên chủ đề ngắn, dễ hiểu: `hello_world`, `math`, `loop`, `function`, `report`
- Dùng hai dạng mở rộng đúng với ngôn ngữ: `.sd` và `.sdpp`
- Chỉ cập nhật README khi đã thêm bài mới hoặc đổi mục lục

## Mục tiêu cuối cùng

Repo nên trở thành một kho học "hữu ích, có trật tự và dễ mở rộng". Người mới có thể bắt đầu từ `examples/` và đi xuyên qua `docs/` mà không bị lạc khi đọc. Đây là kỷ luật tổ chức phần mềm tốt cho dự án giáo dục như Sd/Sd++.
