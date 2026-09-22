# Cách sử dụng bộ dự án

## Môi trường đọc được folder

Mở root dự án, đọc `11 Hướng dẫn làm việc với AI/01 Chỉ dẫn cho AI.md`, sau đó đọc trạng thái, continuity và page spec của nhiệm vụ. Không dùng một file lịch sử v0.1 thay cho trạng thái hiện hành.

## Chat có công cụ tạo ảnh

### Demo A hiện tại

Nên cung cấp/đính kèm theo vai trò:
1. Khôi — CHARACTER IDENTITY.
2. Outfit/prop Khôi nếu cần crop riêng.
3. Thu Anh — CHARACTER IDENTITY.
4. Giảng đường nguồn — GEOMETRY ANCHOR.
5. Ảnh/page look được chọn — STYLE/LIGHTING ANCHOR nếu cần.

Nếu một ảnh đóng nhiều vai trò, phải nói rõ. Không để model tự đoán “ảnh nào để lấy kiến trúc, ảnh nào để lấy ánh sáng”.

Dùng prompt Demo A mới nhất trong 09. Không dùng SVG/layout cũ nếu nó mâu thuẫn page spec.

### Các page khác

Chỉ gửi các reference liên quan đến page đó. Không nạp tất cả asset “cho chắc” vì model có thể trộn chi tiết từ ảnh không liên quan.

## Lettering

Đính kèm đúng artwork/version đã được người dùng duyệt. Artwork là nền bất biến. Sheet/background chỉ dùng để QA khi nghi lệch; không được dùng để tái thiết kế tranh trong bước thêm chữ.

## Khi công cụ không đọc ZIP/folder

Giải nén và tải đúng các file cần. Ghi vai trò từng file. Hỗ trợ loại file, số ảnh và số output phụ thuộc môi trường thực tế; không coi tài liệu này là bảo đảm tính năng.
