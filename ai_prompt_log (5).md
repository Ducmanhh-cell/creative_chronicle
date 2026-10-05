# AI Prompt Log - Refactoring Layout

## Prompt 1: Tìm hiểu CSS Grid cho Mosaic Gallery
- **Câu hỏi**: "Tôi có 1 ảnh lớn bên trái chiếm 2/3 chiều rộng và 2 ảnh nhỏ xếp chồng bên phải. Làm sao dùng CSS Grid để tạo layout này mà không dùng position absolute?"
- **Kết quả ứng dụng**: Sử dụng `display: grid; grid-template-columns: 2fr 1fr;` kết hợp `grid-row: span 2` cho ảnh chính.

## Prompt 2: Tối ưu thanh Author với Bootstrap Flex Utility
- **Câu hỏi**: "Cần căn giữa theo chiều dọc nút Share và Avatar tác giả nằm cùng 1 hàng bằng các class utility d-flex của Bootstrap 5 như thế nào?"
- **Kết quả ứng dụng**: Áp dụng các class `d-flex`, `align-items-center`, `justify-content-between`, và `gap-3` trực tiếp trong HTML, dọn sạch CSS float cũ.

## Prompt 3: Cấu hình Breakpoints cho danh sách bài viết
- **Câu hỏi**: "Cách chia 4 cột bài viết trên Desktop (lg), 2 cột trên Tablet (md) và 1 cột trên Mobile (xs) bằng Bootstrap Grid?"
- **Kết quả ứng dụng**: Sử dụng chuỗi class `col-12 col-md-6 col-lg-3` cho từng `article-card`.
