# Hướng dẫn học Sd / Sd++ (Tiếng Việt)

Chào mừng bạn! Trang này là lộ trình học và mục lục tiếng Việt cho repository. Sd/Sd++ là ngôn ngữ có cú pháp riêng trong dự án, **không phải C/C++**. Bộ thông dịch dùng trong hướng dẫn này nằm trong IDE trình duyệt của repository.

- [English learning guide](../en/README.md)
- [Về trang giới thiệu tiếng Việt](../../README.vi.md)
- [Mục lục tài liệu](../README.md)

## 1. Bắt đầu trong vài phút

1. Mở [`Sd IDE.html`](../../Sd%20IDE.html) bằng trình duyệt hiện đại.
2. Chọn **Mở tệp**, mở một chương trình mẫu `.sd` hoặc `.sdpp` trong `examples/`.
3. Chọn **Chạy** đ��� chạy hoặc **Gỡ lỗi** để xem chương trình từng bước.
4. Với chương trình có `ipt`, nhập dữ liệu trong tab **Nhập liệu** rồi chạy lại.

Các mẫu hiện có:

- [Sd: lời chào](../../examples/sd/01_hello_world.sd) và [phép tính cơ bản](../../examples/sd/02_basic_math.sd).
- [Sd++: lời chào](../../examples/sdpp/01_hello_world.sdpp), [phép tính](../../examples/sdpp/02_basic_math.sdpp), [diện tích hình chữ nhật](../../examples/sdpp/03_rectangle_area.sdpp).
- [Mục lục ví dụ](../../examples/README.md).

## 2. Nhận biết hai dạng mã

| | Sd | Sd++ |
|---|---|---|
| Phần mở đầu chương trình | `sta(main){` | `ssta {` và khối `define [...]` |
| Lệnh in | `iid: sta(pri) ... ed` | `ids.pri: ... $` |
| Khai báo biến | `iid: sta(int x) ... ed` | `iptedt.int x ... $` |
| Kết thúc lệnh | `ed` | `$` |
| Kết thúc tệp | Đóng khối `}` | Kết thúc bằng `##` |
| Phần mở rộng | `.sd` | `.sdpp` |

Đây là quy ước cú pháp mà IDE trong repo xử lý. Nên dùng các chương trình mẫu làm chuẩn khi viết cú pháp mới.

## 3. Lộ trình học gợi ý

1. **Chạy chương trình đầu tiên:** mở ví dụ Hello World và thay nội dung chuỗi.
2. **Biến và phép tính:** xem `02_basic_math` ở mỗi ngôn ngữ; thử đổi giá trị và toán tử.
3. **Điều khiển chương trình:** xem các phần điều kiện và vòng lặp trong tài liệu tham khảo, rồi thêm ví dụ mới thành tệp riêng.
4. **Hàm, cấu trúc dữ liệu và thư viện:** học từ giáo trình/đặc tả gốc; kiểm tra cú pháp trong IDE trước khi mở rộng ví dụ.
5. **Gỡ lỗi:** đặt điểm dừng bằng cách bấm số dòng, chạy debugger và quan sát tab Biến/Vấn đề.

Không nên giả định mọi cú pháp quen thuộc từ ngôn ngữ khác đều được Sd/Sd++ hỗ trợ. Hãy xác minh bằng ví dụ trong repo hoặc tài liệu đặc tả.

## 4. Tài liệu tham khảo

Các tài liệu gốc hiện để ở thư mục gốc để không làm thay đổi liên kết đã có:

- Giáo trình LaTeX: [`Giáo_Trình_Master_...tex`](../../Gia%CC%81o_Tri%CC%80nh_Master_La%CC%A3%CC%82p_Tri%CC%80nh_Sd_va%CC%80_Sd___tu%CC%9B%CC%80_Co%CC%9B_Ba%CC%89n_%C4%91e%CC%82%CC%81n_Na%CC%82ng_Cao.tex).
- Đặc tả kỹ thuật LaTeX: [`Đặc_tả_Kỹ_thuật_...tex`](../../%C4%90a%CC%A3%CC%86c_ta%CC%89_Ky%CC%83_thua%CC%A3%CC%82t_To%CC%82%CC%81i_cao_va%CC%80_Ca%CC%82%CC%89m_nang_Toa%CC%80n_die%CC%A3%CC%82n_Ngo%CC%82n_ngu%CC%9B%83_Sd_va%CC%80_Sd__.tex).
- Ghi chú đặc tả `.txt` và giáo trình PDF: xem danh sách tệp ở thư mục gốc; PDF hiện tên `giaotrinhsd:sdpp.pdf`.
- [Hướng dẫn đọc mã IDE tiếng Việt](../../CODE_GUIDE.md).

## 5. Tạo và tổ chức bài học mới

- Sd đặt trong `examples/sd/`, tên dạng `04_vong_lap.sd`.
- Sd++ đặt trong `examples/sdpp/`, tên dạng `04_vong_lap.sdpp`.
- Mỗi tệp là một bài/chương trình độc lập; dùng tên không dấu, chữ thường, có số thứ tự.
- Cập nhật bảng trong README của thư mục tương ứng khi thêm bài.
- Không đổi phần mở rộng hoặc trộn dấu kết thúc `ed`, `$`, `##` giữa hai cú pháp.

## 6. Sửa lỗi thường gặp

- **IDE báo lỗi cú pháp:** kiểm tra phần mở đầu/đóng khối và dấu kết thúc của đúng ngôn ngữ.
- **Không thấy đầu ra:** kiểm tra đã chọn đúng tệp và bấm Chạy; xem tab Vấn đề nếu có lỗi.
- **Lệnh nhập thiếu dữ liệu:** nhập thêm dòng trong tab Nhập liệu.
- **Tìm tệp:** dùng mục lục [`docs/README.md`](../README.md) hoặc tìm kiếm repository trên GitHub.
