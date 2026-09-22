# Giảng đường

Nguồn kịch bản MD T01: giảng đường đại học chiều muộn, nắng xiên qua cửa kính, bảng chiếu ở đầu lớp. Demo A đã khóa Khôi ở **hàng ghế đầu ngoài cùng**.

## Geometry anchor
`01 Ảnh nguồn/Giảng đường.png` là **GEOMETRY ANCHOR**. Chỉ khóa những gì thật sự quan sát được trong ảnh.

### Quan sát được
- Giảng đường bậc thang; các hàng sau cao dần.
- Bàn học là dãy **thẳng và song song**, không vòng cung.
- Bậc sàn + mép bàn tạo perspective diagonal nhất quán.
- Khi đứng FRONT nhìn BACK, cầu thang quan sát được chạy dọc **mép phải khối ghế**.
- Khu giảng viên ở tầng thấp phía FRONT.
- Có nhiều cụm cửa sổ/cửa kính quan sát được; không rút thành một “WINDOW-SIDE” duy nhất.
- Bảng/khu giảng viên/cầu thang/các dãy bàn là landmark đã quan sát được.

### Không được tự khóa
**Cửa ra vào chưa được geometry anchor hiện tại xác nhận rõ.** Nếu panel không cần cửa, ưu tiên không vẽ cửa hơn là tự phát minh vị trí/kích thước.

Quy tắc: **không quan sát được ≠ được phép bịa cho đầy khung**.

## Spatial map Demo A
- FRONT = bảng/khu giảng viên.
- BACK = hàng ghế cao dần.
- RIGHT-STAIR = cầu thang ở mép phải khối ghế khi nhìn FRONT→BACK.
- WINDOW-ZONES = giữ các cụm cửa sổ/cửa kính thực sự thấy.
- ENTRY-DOOR = UNRESOLVED / không bắt buộc hiển thị.
- KHOI-SEAT = hàng ghế đầu ngoài cùng.

## Lighting
Giữ chiều muộn vàng ấm, nắng xiên, highlight ấm, bóng mềm có hướng, nền xanh/xám trung tính. Lighting không được tái thiết kế geometry.

## Crowd
Không clone rõ; không tự tạo reaction character; A3 phần lớn quần chúng vẫn hướng FRONT.

Chưa có artwork/background Demo A nào được người dùng duyệt.


## World-space và phép chiếu camera cho Demo A

Để tránh lỗi "giữ landmark cùng bên màn hình dù camera quay 180°", dùng hệ trục cố định:

- Trục Y: FRONT → BACK.
- Trục X dương: phía RIGHT-STAIR khi đứng ở FRONT nhìn về BACK.
- Khôi ngồi ở hàng đầu, ghế ngoài cùng sát phía RIGHT-STAIR.

Quy tắc chiếu:
- **A1: camera ở phía BACK nhìn về FRONT.** Vì camera quay ngược chiều trục Y, phía world RIGHT-STAIR phải chiếu sang **screen-left**. Khôi ở ghế sát RIGHT-STAIR cũng phải nằm về phía screen-left của khối ghế, không screen-right.
- **A3: camera ở phía FRONT nhìn về BACK.** Phía world RIGHT-STAIR chiếu sang **screen-right**. Khôi ở ghế sát RIGHT-STAIR nằm ngay bên trái cầu thang hoặc vùng screen-right của khối ghế.

Cùng một world-side khi camera quay 180° **không được giữ cùng screen-side**. Nếu A1 và A3 đều đặt cầu thang ở screen-right, topology đã sai dù từng panel riêng lẻ trông đẹp.
