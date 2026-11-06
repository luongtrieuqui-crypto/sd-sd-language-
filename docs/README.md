# Mục lục và cách tổ chức tệp

Trang này là bản đồ để tìm, mở và chỉnh sửa nội dung trong repository. Các tài liệu có tên dài hoặc dấu tiếng Việt hiện được giữ nguyên tại thư mục gốc để bảo toàn liên kết đã có.

## Bản đồ nhanh

| Bạn muốn... | Mở tệp/thư mục |
|---|---|
| Soạn/chạy/gỡ lỗi chương trình | [`Sd IDE.html`](../Sd%20IDE.html) |
| Xem chương trình Sd mẫu | [`examples/sd/`](../examples/sd/) |
| Xem chương trình Sd++ mẫu | [`examples/sdpp/`](../examples/sdpp/) |
| Đọc hướng dẫn mã nguồn tiếng Việt | [`CODE_GUIDE.md`](../CODE_GUIDE.md) |
| Đọc hướng dẫn mã nguồn tiếng Anh | [`CODE_GUIDE.en.md`](../CODE_GUIDE.en.md) |
| Xem giáo trình LaTeX | [Giáo trình `.tex`](../Gia%CC%81o_Tri%CC%80nh_Master_La%CC%A3%CC%82p_Tri%CC%80nh_Sd_va%CC%80_Sd___tu%CC%9B%CC%80_Co%CC%9B_Ba%CC%89n_%C4%91e%CC%82%CC%81n_Na%CC%82ng_Cao.tex) |
| Xem đặc tả kỹ thuật LaTeX | [Đặc tả `.tex`](../%C4%90a%CC%A3%CC%86c_ta%CC%89_Ky%CC%83_thua%CC%A3%CC%82t_To%CC%82%CC%81i_cao_va%CC%80_Ca%CC%82%CC%89m_nang_Toa%CC%80n_die%CC%A3%CC%82n_Ngo%CC%82n_ngu%CC%9B%83_Sd_va%CC%80_Sd__.tex) |
| Tìm ghi chú đặc tả dạng văn bản | [Tài liệu `.txt`](../Ta%CC%80i_lie%CC%A3%CC%82u_%C4%90a%CC%A3%CC%86c_ta%CC%89_Master_%C4%90a%CC%A3%86c_ta%CC%89_Ky%CC%83_thua%CC%A3%CC%82t_Ngo%CC%82n_ngu%CC%9B%83_Sd_va%CC%80_Sd__.txt) |
| Xem giáo trình PDF | [`giaotrinhsd:sdpp.pdf`](../giaotrinhsd:sdpp.pdf) |

## Nội dung hiện có ở thư mục gốc

| Tệp | Mục đích / khuyến nghị |
|---|---|
| `Sd IDE.html` | IDE độc lập trên trình duyệt, bao gồm giao diện, bộ ph��n tích và máy ảo. |
| `sdform.sd`, `shortsd.sd` | Ví dụ Sd ban đầu; giữ nguyên để tương thích, ví dụ mới đặt trong `examples/sd/`. |
| `form opencode sd`, `formopen code sd++` | Tệp mẫu/nháp ban đầu; ví dụ mới đặt trong `examples/` với phần mở rộng `.sd` hoặc `.sdpp`. |
| `Giáo_Trình_Master_...tex` | Giáo trình LaTeX. Giữ nguyên tên hiện tại; dùng mục lục ở trên để mở. |
| `Đặc_tả_Kỹ_thuật_...tex` | Tài liệu đặc tả LaTeX. |
| `Tài_liệu_Đặc_tả_...txt` | Đặc tả/ghi chú dạng văn bản. |
| `giaotrinhsd:sdpp.pdf` | Giáo trình PDF. |
| `IMG_0774.jpeg` | Hình ảnh tham khảo. |
| `README.md`, `README.vi.md`, `README.en.md` | Trang giới thiệu dự án theo ngôn ngữ. |
| `CODE_GUIDE.md`, `CODE_GUIDE.en.md` | Hướng dẫn đọc mã nguồn. |

## Quy ước để thêm tệp mới

- Chương trình Sd: `examples/sd/<số-thứ-tự>_<chủ-đề>.sd`.
- Chương trình Sd++: `examples/sdpp/<số-thứ-tự>_<chủ-đề>.sdpp`.
- Tài liệu mới: đặt trong `docs/` và dùng tên ngắn, ASCII, có gạch nối; ví dụ `language-reference.md`.
- Tài nguyên như hình ảnh: đặt trong `assets/` nếu bổ sung tài nguyên mới.
- Tên tệp nên viết thường, không dấu, không khoảng trắng; giữ tên cũ khi đổi tên có thể làm hỏng liên kết hiện hữu.
- Mỗi ví dụ nên là một chương trình độc lập, có tên mô tả nội dung. Cập nhật README của thư mục tương ứng khi thêm bài mới.

## Tìm kiếm và chỉnh sửa

- Dùng tìm kiếm của GitHub để tìm theo tên tệp hoặc nội dung; từ trang repository có thể nhấn `t` để tìm tệp.
- Khi sửa ví dụ, chỉ cần mở tệp `.sd`/`.sdpp` tương ứng trong IDE hoặc trình soạn thảo văn bản; các ví dụ không phụ thuộc lẫn nhau.
- Không đổi phần mở rộng hoặc dấu kết thúc lệnh của một ngôn ngữ sang cú pháp của ngôn ngữ kia.
- Các thư mục và tài liệu được phân loại theo mục đích; không gom mã nguồn, tài liệu và tài nguyên vào cùng một tệp.
