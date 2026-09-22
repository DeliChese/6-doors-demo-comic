# Trạng thái hiện tại

| Hạng mục | Trạng thái | Việc tiếp theo |
|---|---|---|
| Full-tree và tài liệu | Đã soạn v0.1, đang đồng bộ nguồn hình | Tiếp tục cập nhật theo asset thực tế |
| Nguồn kịch bản | Đã nhập | Giữ nguyên, cập nhật có phiên bản |
| Khôi | Hoạt động, Asset Package Cấp A; đã có sheet gốc | Tiếp tục chuẩn hóa crop nhận diện xuyên suốt |
| Thu Anh | Vai phụ Demo A; đã có sheet người dùng cung cấp | Giữ continuity A2/A4; chưa nâng thành Cấp A |
| Bối cảnh Giảng đường | Đã có ảnh nguồn | GEOMETRY ANCHOR đã audit; không suy landmark ngoài khung |
| Những nhân vật khác | Chưa kích hoạt | Không tự mở package |
| 8 shot continuity | Đã soạn spec, chưa có ảnh | Tạo theo nhu cầu kiểm thử |
| Demo A | **Đang chỉnh sửa**; spec đã audit nhưng pipeline cũ cho thấy full-render quá sớm gây lãng phí | Chạy Preflight P1–P5, chỉ PASS mới full render |
| Page B | Có layout và prompt, chưa có tranh | Chờ sau khi Demo A qua cổng |
| Page C | Bài thử chuyển cảnh tùy chọn | Dùng nếu cần test bước chân và SFX |
| 1–2 trang tranh duyệt đầu vào | Chưa có bản đạt duyệt | Chỉ chuyển sang lettering sau khi người dùng duyệt tranh |
| Balloon, thoại, SFX | Có quy trình, bảng chữ và prompt | Chưa thực hiện trên Demo A |
| Duyệt cuối | Chưa có | Người dùng duyệt sau kiểm |

## Quyết định đã khóa cho Demo A

1. Outfit M01 của Khôi: dùng đúng outfit trên sheet hiện tại.
2. Vị trí Khôi: hàng ghế đầu ngoài cùng.
3. Trong lớp Khôi không đeo ba lô trên vai; ba lô đặt tự nhiên cạnh/chân ghế.
4. Nhịp: A1 giơ tay khi Thu Anh đang giảng → A3 hạ tay và hỏi → A4 Thu Anh lắng nghe/phản hồi.
5. A3 dùng reverse shot từ phía trước Khôi, nhìn về cuối lớp; không thấy bục giảng/bảng/Thu Anh.
6. A3 lớn hơn A4 để dành vùng balloon cho câu hỏi của Khôi.
7. A2/A4 phải thay đổi góc máy/pose thực sự, không chỉ thay bàn tay.

## QA artwork thử gần nhất

Bản thử chưa được duyệt. Các lỗi đã log gồm: trục nhìn A3; geometry A1/A3; hàng bàn vòng cung; crowd clone/reaction turn; ba lô/đồng hồ; landmark teleport; A4 quá lớn/lặp góc Thu Anh. Audit cuối bổ sung rule: phần kiến trúc không quan sát được không được tự phát minh. Bản thử mới nhất tiếp tục FAIL ở phép chiếu 180°: world RIGHT-STAIR bị giữ cùng screen-side giữa A1/A3; đã bổ sung world-space projection rule. Những lỗi này là blocker trước lettering.

Không đặt ảnh vào mục Đã duyệt chỉ vì AI tự đánh giá là đẹp.


## Quy trình production mới bắt buộc

Từ 23-09-2026, mọi page nhiều panel dùng:
1. `02 Quy chuẩn dự án/06 Quy chuẩn dựng hình và đạo diễn panel Manhwa.md`
2. `09 Thiết kế trang và prompt/00 Pipeline tiền kỳ một trang Manhwa.md`
3. `12 Kiểm thử và duyệt/04 Checklist Preflight trước Full Render.md`

**Không full-render trực tiếp từ prompt page nếu chưa PASS structural preflight.**
Ba lỗi structure lặp cùng loại được coi là pipeline failure: dừng generation và sửa scene model/camera/layout trước.
