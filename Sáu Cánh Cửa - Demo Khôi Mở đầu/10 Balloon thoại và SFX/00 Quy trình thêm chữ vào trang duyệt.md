# Thêm balloon thoại và SFX vào 1–2 trang đã duyệt

Phạm vi: AI nhận artwork đã duyệt, bảng chữ và quy tắc đặt chữ để làm bản có chữ. Không cần tạo lại trang từ mô tả. Một lần giao việc có thể gồm một hoặc hai trang độc lập; nếu công cụ chỉ trả một ảnh mỗi lượt, xử lý tuần tự và giữ hai đầu ra riêng.

## Bước 1 Nhận trang

Copy 1–2 ảnh đã được người dùng duyệt tranh vào `01 Trang tranh đã duyệt đầu vào`. Điền tên thật, kích thước, mã page, phiên bản và bằng chứng duyệt trong phiếu nhận. Giữ bản đầu vào nguyên trạng. Nếu page không phải A/B/C, lập bảng chữ từ đúng đoạn nguồn của page đó.

## Bước 2 Khóa nội dung chữ

Chọn bảng A, B hoặc C tương ứng. Chỉ chữ ở cột “nội dung hiển thị” mới xuất hiện trên tranh. Tên nhân vật, mã balloon, ghi chú diễn xuất và tọa độ không được render. Đánh dấu dòng được chọn. Không tự thêm SFX cho trang không có âm thanh chỉ để dùng hết tính năng.

## Bước 3 Lập bản đồ chữ

AI xem đúng trang đã duyệt, đánh dấu vị trí và vùng cấm che theo `03 Vùng chữ và vùng bảo vệ`. Đề xuất thứ tự đọc và kích thước balloon dựa trên lượng chữ thật. Tọa độ demo chỉ khởi điểm, không áp máy móc lên ảnh có layout khác. Nếu không đủ chỗ, ghi cách chỉnh placement hoặc chia balloon cùng câu, giữ nguyên thứ tự chữ; không tóm tắt lời thoại.

## Bước 4 Thực hiện

Dùng prompt thêm chữ một trang hoặc hai trang. Nếu công cụ hỗ trợ mask, dùng vùng cho phép gồm balloon, đuôi và SFX; kiểm màu mask theo công cụ, không mặc định trắng/đen có cùng ý nghĩa. Chỉ chỉnh vào bản copy, yêu cầu giữ nguyên kích thước, panel và artwork ngoài vùng chữ. Công cụ tạo ảnh có thể vẫn vẽ lại chi tiết; yêu cầu bảo toàn không phải bảo đảm kỹ thuật.

## Bước 5 Kiểm và sửa

So chữ với bảng nguồn từng ký tự, rồi kiểm mắt, kính, tay, áo, background và đường panel bằng so sánh cạnh nhau hoặc chồng ảnh đồng kích thước. OCR chỉ hỗ trợ, không thay đọc trực tiếp. Nếu có thay đổi ngoài vùng chữ, không duyệt bản đó. Sửa hẹp hoặc dùng lớp chữ vector trên artwork gốc trong trình dàn trang; AI vẫn có thể soạn placement và lớp chữ, không cần tái sinh artwork.

## Bước 6 Duyệt và xuất

Ghi duyệt chữ trên đúng phiên bản artwork. Lưu bản kết hợp vào `07 Trang có chữ đã duyệt`, file lớp tách nếu có ở `08 Lớp chữ và tệp chỉnh sửa`; bản xuất sang `08 Xuất thử/03 Bản xuất có chữ`. Nếu công cụ chỉ tạo raster, ghi rõ không có layer thật; không đặt đuôi PSD để giả file nhiều lớp.

Hai trang không được ghép thành một canvas trừ khi yêu cầu rõ là spread. Đầu vào đã có chữ: ghi giữ/thay/xóa chính xác từng vùng, không chồng balloon mới lên chữ cũ chưa xử lý.
