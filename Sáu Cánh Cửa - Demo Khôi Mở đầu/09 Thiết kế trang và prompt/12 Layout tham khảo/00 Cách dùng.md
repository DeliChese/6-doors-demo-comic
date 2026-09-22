# Layout tham khảo

SVG chỉ là **LAYOUT ANCHOR**, không phải artwork, không phải canon bối cảnh và không phải bằng chứng duyệt.

## Thứ tự ưu tiên

1. Page spec hiện hành.
2. Quyết định người dùng mới nhất.
3. SVG layout tương ứng phiên bản hiện hành.
4. Ví dụ/layout lịch sử.

Nếu SVG mâu thuẫn page spec, **page spec thắng** và SVG phải được cập nhật trước khi dùng lại.

## Demo A hiện hành

Demo A không còn lưới 2×2 bằng nhau:
- A1: panel establishing lớn ở trên trái.
- A2: panel Thu Anh nhỏ hơn ở trên phải.
- A3: panel chính lớn nhất ở dưới trái.
- A4: panel phản ứng nhỏ ở dưới phải.

A3 lớn hơn A4 để giữ không gian cho balloon câu hỏi. Nhãn A1/A2/A3/A4 chỉ là hướng dẫn, không render vào tranh.

Tọa độ SVG là footprint dàn trang, **không quyết định camera/geometry trong panel**. Camera và spatial logic phải đọc ở `02 Demo A Giảng đường.md`.
