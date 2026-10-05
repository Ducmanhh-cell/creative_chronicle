# Báo Cáo Refactoring Layout: "CreativeChronicle"

## 1. Tác hại của `position: absolute` đối với Responsive Design
Thuộc tính `position: absolute` đưa phần tử ra khỏi luồng tài liệu thông thường (Normal Document Flow). Do đó, phần tử cha chứa nó không thể tự động tính toán chiều cao dựa trên các phần tử con. 

Khi áp dụng chiều cao cố định (`height: 400px`) cho khu vực Mosaic Gallery trên màn hình nhỏ, các phần tử con không thể thu hẹp đúng tỉ lệ, dẫn đến hiện tượng trào nội dung (overflow) hoặc che đè thảm họa lên đoạn văn bản nằm bên dưới.

## 2. CSS Grid - Giải pháp cứu cánh cho Bố cục 2D
CSS Grid giải quyết triệt để bài toán bố cục 2 chiều (hàng và cột) mà không cần can thiệp vào `position` hay tính toán pixel thủ công:
- **Tự động đẩy luồng tài liệu**: Khung chứa (`.mosaic-gallery`) tự co giãn chiều cao chuẩn xác theo kích thước ô, giữ đoạn văn bản phía dưới luôn ở đúng vị trí.
- **Linh hoạt điểm ngắt (Breakpoints)**: Bằng cách kết hợp `grid-template-columns` và `@media`, thư viện ảnh chuyển đổi mượt mà từ dạng khảm bất đối xứng 2 cột (Desktop) sang dạng xếp chồng 1 cột (Mobile) chỉ với vài dòng mã CSS ngắn gọn.
