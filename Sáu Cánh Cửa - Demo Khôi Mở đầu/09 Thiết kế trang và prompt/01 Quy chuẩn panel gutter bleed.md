# Quy chuẩn trang demo

| Khái niệm | Nghĩa dùng trong dự án |
|---|---|
| Panel | Ô tranh mô tả một khoảnh khắc hoặc nhịp |
| Gutter | Khoảng cách giữa panel, không phải phần bị cắt khi in |
| Bleed | Vùng hình vượt đường cắt ở bản in; hình chạm mép ebook không tự tạo bleed in |
| Full bleed | Artwork chạy đến mọi mép trang; khi in cần phần dư ngoài đường cắt |
| Splash | Một hình chi phối trang, có thể có lề; không đồng nghĩa bắt buộc full bleed |
| Inset | Panel nhỏ đặt chồng trên hình lớn, có thứ tự đọc rõ |
| Safe area | Vùng an toàn cho chữ và chi tiết quan trọng |

Thông số demo hiện tại: trang dọc 2:3, 1600 × 2400 px; lề khoảng 4%, gutter khoảng 2% chiều rộng, viền scale theo kích thước đích. Đây là thông số demo, không phải canon tác phẩm.

Đọc trái sang phải, trên xuống dưới.

## Luật quan trọng về layout

**Page spec hiện hành của từng trang có ưu tiên cao hơn ví dụ layout tổng quát hoặc SVG cũ.**

Demo A hiện là **4 panel bất đối xứng**, không còn được mô tả là lưới 2×2 bằng nhau:
- A1 rộng hơn A2 ở hàng trên nếu cần establishing;
- A3 là panel chính ở hàng dưới;
- A4 nhỏ hơn A3;
- A3 phải đủ vùng âm cho balloon câu hỏi của Khôi.

Không ép hai panel bằng nhau chỉ để “đẹp lưới” nếu làm mất nhịp kể hoặc vùng lettering.

Demo B là splash/spread test theo spec riêng. Demo C dùng nền lớn + inset theo spec riêng. Không lấy footprint của B/C áp sang A.

Chừa khoảng composition cho chữ trước khi vẽ, chưa vẽ balloon rỗng. Không đặt vùng chữ lên mặt, kính, bàn tay hành động, biểu tượng cửa hoặc chi tiết cốt truyện. “Chừa chỗ” không có nghĩa tạo một mảng trắng thô.
