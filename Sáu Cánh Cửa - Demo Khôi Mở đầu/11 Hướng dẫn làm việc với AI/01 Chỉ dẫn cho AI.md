# Chỉ dẫn cho AI làm dự án

Đọc theo thứ tự: `00 Bắt đầu tại đây.md` → `00 Trạng thái hiện tại.md` → quy chuẩn dự án → nội dung xuyên suốt → canon/asset liên quan → **page spec hiện hành của nhiệm vụ** → prompt hiện hành. Không cần nạp toàn bộ kịch bản nếu đã có đoạn nguồn đúng.

## Thứ tự ưu tiên khi có xung đột

1. Quyết định mới, rõ ràng của người dùng.
2. Kịch bản hiện hành về sự kiện/nội dung.
3. Canon hình/asset đã được người dùng duyệt.
4. Page spec + continuity/change log hiện hành.
5. Quy chuẩn chung.
6. Ví dụ/layout cũ/art direction đề xuất.

**Tài liệu lịch sử v0.1, SVG cũ hoặc ảnh AI cũ không được thắng page spec mới.**

Nếu gặp hai câu chỉ dẫn mâu thuẫn, không “pha trung bình” hai câu. Xác định cái nào mới/cụ thể hơn; nếu vẫn không xác định được và ảnh hưởng lớn tới output thì báo blocker.

## Package hiện hành

- Khôi: Asset Package Cấp A, dùng xuyên mạch truyện.
- Thu Anh: package tối thiểu vai phụ cho Demo A để giữ continuity.
- Không tự mở package hàng loạt cho các nhân vật khác.

## Reference phải được gán vai trò

Mở/xem ảnh thật. Không suy từ filename.

- CHARACTER IDENTITY: mặt/tóc/tỷ lệ.
- OUTFIT/PROP: quần áo/đạo cụ.
- GEOMETRY ANCHOR: topology, landmark, spacing, kiến trúc.
- STYLE/LIGHTING ANCHOR: mood/rendering/hướng sáng.
- LAYOUT ANCHOR: footprint panel.

Không để một ảnh style đẹp tự thay geometry. Không dùng nhân vật quần chúng từ background reference làm character canon. **Chỉ khóa chi tiết thật sự quan sát được trong reference; phần ngoài khung phải ghi không quan sát được, không tự hoàn thiện bằng suy đoán.**

## Khi tạo page

- đọc page spec mới nhất;
- dựng spatial map nếu có nhiều góc trong cùng bối cảnh; spatial map chỉ chứa landmark quan sát được/source xác nhận;
- mỗi panel phải ghi camera ở đâu, nhìn về đâu, background phải/cấm thấy gì;
- giữ screen direction và vị trí vật lý props;
- chừa vùng lettering theo nội dung sau này;
- không ghép 8 continuity shot thành một page.

Nếu page có lỗi cục bộ, ưu tiên sửa panel/vùng. Nếu topology/phối cảnh sai nhiều panel, dừng và sửa geometry/spec trước thay vì tái sinh mù.

## Duyệt và lettering

Không tự chuyển bản thử thành bản duyệt. Chỉ letter trên đúng artwork/version người dùng đã duyệt. Khi thêm chữ, đọc quy trình 10, giữ source artwork và đúng mapping page-text.

Đọc nguồn pháp luật như văn bản biên tập, không tự chứng nhận chính xác pháp lý. Nếu nhiệm vụ là thẩm định/sửa luật, phải dùng nguồn có thẩm quyền và ghi phiên bản/ngày.

Ghi prompt, reference thực tế, output, lỗi, cách sửa và quyết định vào nhật ký. Không có image tool thì không báo đã tạo ảnh. Không đọc được folder thì yêu cầu đúng file cần thiết, không giả vờ đã đọc ZIP.


## Quy tắc chống hallucination không gian
Nếu reference chỉ cho một góc của phòng, AI không được tự coi phần không thấy là canon. Khi page không cần một landmark chưa quan sát, ưu tiên **không hiển thị** hơn là phát minh. Nếu landmark bắt buộc cho hành động, cần reference/quyết định staging hoặc ghi rõ đó là ĐỀ XUẤT.
