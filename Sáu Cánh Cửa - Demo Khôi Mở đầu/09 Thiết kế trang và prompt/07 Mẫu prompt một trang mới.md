# Mẫu prompt một trang

Điền đủ rồi mới gửi; không dùng mẫu này để ghi đè prompt A/B/C hiện hành.

1. **Mã trang + nguồn:** …
2. **Loại trang + kích thước/tỉ lệ:** …
3. **Reference thực tế + version + vai trò:** CHARACTER IDENTITY / OUTFIT-PROP / GEOMETRY / STYLE-LIGHTING / LAYOUT.
4. **Canon nhân vật + outfit đã khóa:** …
5. **Bối cảnh:** time of day / FRONT-BACK / cửa / cửa sổ / cầu thang-lối đi / landmark cố định / geometry anchor.
6. **Lighting:** hướng sáng, nhiệt độ màu, nguồn sáng chính; ghi rõ reference nào chỉ dùng cho style/light.
7. **Layout:** panel footprint, gutter, thứ tự đọc, panel nào ưu tiên diện tích và vì sao.
8. **Mỗi panel:** camera nằm ở đâu / nhìn về đâu / nhân vật quay hướng nào / hành động / biểu cảm / đạo cụ / background phải thấy / background cấm thấy / vùng chữ.
9. **Continuity:** props, tay, phụ kiện, vị trí vật lý, screen direction, crowd behavior.
10. **Negative constraints:** các lỗi đã gặp phải cấm lặp.
11. **Chế độ:** tranh không chữ / thêm chữ vào tranh duyệt / sửa riêng panel-vùng.
12. **Đầu ra + trạng thái:** một page/spread; tên version; chỉ Đang thử nếu chưa có duyệt người dùng.

## Trước khi generation

Nếu page có nhiều góc máy trong cùng một không gian, phải dựng **spatial map bằng chữ** trước. Không dùng câu mơ hồ kiểu “giữ bối cảnh giống reference” mà không nói cái gì cần giữ.

Nếu hai reference có mục tiêu khác nhau, không trộn:
- geometry lấy từ geometry anchor;
- ánh sáng lấy từ lighting anchor;
- mặt/outfit lấy từ character reference.

Nếu tool không đọc được thư mục, prompt nguyên văn phải chứa spec cần thiết và các ảnh phải được đính kèm thật. Không chỉ nói “làm theo project”.
