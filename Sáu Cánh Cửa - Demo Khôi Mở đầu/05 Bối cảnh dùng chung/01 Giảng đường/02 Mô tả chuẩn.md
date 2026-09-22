# Giảng đường

Nguồn kịch bản MD T01: giảng đường đại học chiều muộn, nắng xiên qua cửa kính, bảng chiếu ở đầu lớp; nữ giảng viên khoảng 45 tuổi. Quyết định mới của người dùng đã thay staging Khôi từ dãy cuối thành **hàng ghế đầu ngoài cùng** cho Demo A.

## Reference hình hiện có

Ảnh nguồn giảng đường đã được người dùng đưa vào `01 Ảnh nguồn`. Ảnh này là **GEOMETRY ANCHOR** cho Demo A: dùng để khóa kiến trúc và quan hệ không gian, không chỉ làm gợi ý phong cách.

### Hình học phải giữ

- Giảng đường dạng bậc thang: các hàng sau cao dần so với hàng trước.
- Bàn học là các dãy **thẳng và song song theo tầng**, không uốn thành vòng cung/amphitheatre.
- Các mép bàn và bậc sàn tạo hệ đường chéo phối cảnh nhất quán khi đổi camera.
- Có lối/cầu thang đi lên theo cạnh giảng đường như reference. Khi camera đảo chiều, vị trí biểu kiến trái/phải có thể đổi theo phép chiếu, nhưng **cùng một cầu thang không được tự nhảy sang phía đối diện của phòng**.
- Khu vực giảng viên ở tầng thấp phía trước; các hàng sinh viên nâng dần về phía sau.
- Cửa, cửa sổ, bảng, bục/bàn giảng viên và cầu thang phải được hiểu như các landmark của **một phòng duy nhất**. Không tái thiết kế từng panel thành một lớp khác.
- Kích thước cửa phải hợp tỷ lệ người; không thu nhỏ thành cửa phụ bé bất thường.

## Orientation map bắt buộc trước generation

Mỗi page spec dùng giảng đường phải khai báo tối thiểu:

1. FRONT = phía bảng/bục giảng viên.
2. BACK = phía các hàng ghế cao dần.
3. SIDE-STAIR = cạnh có cầu thang đi lên theo reference.
4. WINDOW-SIDE = cạnh có hệ cửa sổ chính theo reference.
5. DOOR = landmark cửa ra vào đã chọn; một vị trí vật lý duy nhất.
6. KHOI-SEAT = hàng ghế đầu ngoài cùng.

Nếu crop/góc máy làm một landmark không quan sát được, ghi **không quan sát được**; không được tự sinh landmark sang phía còn lại để “lấp chỗ trống”.

## Ánh sáng / look anchor cho Demo A

Người dùng chọn look của các bản thử gần đây làm **STYLE/LIGHTING ANCHOR**, không thay geometry anchor:

- chiều muộn ấm;
- nắng vàng xiên qua cửa sổ;
- highlight ấm trên tóc/da/cạnh bàn;
- bóng đổ mềm nhưng có hướng;
- nền xanh/xám trung tính của lớp giúp ánh nắng ấm nổi lên;
- manhwa màu bán hiện thực, sạch, điện ảnh; không chuyển thành 3D render.

Nguyên tắc: **geometry lấy từ ảnh nguồn giảng đường; tone ánh sáng có thể lấy từ look bản thử được người dùng thích.** Không để style đẹp làm thay đổi kiến trúc.

## Quần chúng

- Quần chúng phục vụ scale/depth, không trở thành nhân vật phản ứng nếu kịch bản không yêu cầu.
- Tránh clone: không đặt hai người gần nhau có cùng tóc + cùng khuôn mặt + cùng pose + cùng silhouette.
- Cho biến thiên có kiểm soát về giới tính trình bày, kiểu tóc, kính, dáng ngồi và chi tiết mặc đồng phục.
- Vẫn giữ cùng hệ đồng phục/trường hư cấu; không biến thành nhiều dress code khác nhau.
- Trong A3, sinh viên phía sau chủ yếu hướng về FRONT; không quay hẳn lại nhìn Khôi nếu không có beat phản ứng trong kịch bản.

## Trạng thái

Geometry anchor: đã có nguồn hình và được dùng cho Demo A. Look ánh sáng: đã có hướng người dùng chọn từ bản thử. Chưa coi một artwork page nào là Đã duyệt.
