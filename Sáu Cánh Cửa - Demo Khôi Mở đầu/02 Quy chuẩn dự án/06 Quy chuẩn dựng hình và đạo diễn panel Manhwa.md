# Quy chuẩn dựng hình và đạo diễn panel Manhwa

Phiên bản 1.0 — **PRODUCTION STANDARD**, không phải canon nội dung. Áp dụng cho Demo M01 và tái sử dụng cho các chương sau trừ khi page spec ghi ngoại lệ.

Mục tiêu: buộc quy trình AI/họa sĩ làm việc theo cách của một ê-kíp comic chuyên nghiệp: **dựng đúng trước, đẹp sau; đo bằng quan hệ không gian; đạo diễn panel trước khi render; tái sử dụng set/camera/asset thay vì phát minh lại mỗi lần.**

---

## 1. Sáu nguyên tắc không được phá

1. **Một scene = một world model.** Nhiều panel là nhiều camera nhìn cùng một không gian, không phải nhiều phiên bản căn phòng.
2. **Structure trước rendering.** Perspective, tỷ lệ, blocking, pose, prop, negative space phải đạt trước khi tô chi tiết.
3. **Panel kể chuyện, không phải gallery.** Mỗi panel phải có beat, mục tiêu thị giác và quan hệ với panel trước/sau.
4. **Không quan sát được thì không tự biến thành canon.** Phần ngoài reference là UNKNOWN cho tới khi source/spec xác nhận.
5. **Giữ world-space, không giữ screen-space.** Camera đảo thì landmark có thể đổi trái/phải trên màn hình nhưng không đổi vị trí vật lý.
6. **Full render là bước cuối.** Không tiêu lượt render chất lượng cao để kiểm một lỗi có thể phát hiện bằng sơ đồ, silhouette hoặc blockout.

---

## 2. Đơn vị đo sản xuất

Không bịa kích thước centimet nếu source không cho. Dùng **đơn vị tương đối**.

### 2.1 Nhân vật làm thước
- Chọn một full-body reference đã chấp nhận làm mốc, ký hiệu chiều cao nhân vật là **H**.
- Tất cả tỷ lệ môi trường được ước lượng theo H hoặc theo chính landmark trong geometry reference.
- Khi reference có người/bàn/cửa cùng khung, ưu tiên đo tỷ lệ trực tiếp từ ảnh hơn mọi heuristic.

### 2.2 Heuristic chỉ dùng khi source thiếu
Các tỷ lệ dưới đây là **ĐỀ XUẤT kỹ thuật**, không phải canon:
- người trưởng thành bán hiện thực: khoảng 7–8 đầu;
- mặt bàn học/bàn làm việc: khoảng 0.40–0.45H;
- mặt ghế: khoảng 0.24–0.28H;
- cửa đi thông thường: khoảng 1.10–1.20H;
- bậc cầu thang: chiều cao mỗi bậc khoảng 0.09–0.11H.

Nếu heuristic xung đột reference, **reference thắng**.

### 2.3 Measurement sheet
Bối cảnh tái sử dụng phải có bảng:
- landmark;
- tỷ lệ tương đối;
- khoảng cách tương đối;
- độ cao;
- quan hệ trái/phải trước/sau;
- trạng thái: OBSERVED / INFERRED-PROPOSAL / APPROVED.

Không dùng giá trị INFERRED-PROPOSAL như canon cho page sau nếu chưa được khóa.

---

## 3. Set Bible cho mỗi bối cảnh tái sử dụng

Trước khi bối cảnh dùng ở nhiều panel/page, tạo **SET BIBLE** tối thiểu.

### 3.1 Floor plan
Phải xác định:
- FRONT / BACK;
- LEFT / RIGHT theo world-space;
- cửa/lối đi nếu quan sát được;
- cửa sổ;
- cầu thang;
- đồ nội thất lớn;
- vị trí nhân vật quan trọng;
- vùng không quan sát được.

### 3.2 Elevation / height logic
Ghi:
- mặt sàn;
- bậc cao thấp;
- trần;
- chiều cao bàn/ghế;
- landmark cao/thấp;
- vật nào che vật nào.

Không cần bản CAD; sơ đồ chữ + block diagram đủ nếu rõ topology.

### 3.3 Landmark register
Mỗi landmark có ID:
- BG-L01, BG-L02...
- tên;
- vị trí world-space;
- source;
- panel nào nhìn thấy;
- panel nào không thể nhìn thấy.

### 3.4 Camera map
Mỗi camera có:
- CAM-ID;
- tọa độ tương đối;
- hướng nhìn;
- eye level;
- FOV class: WIDE / NORMAL / PORTRAIT;
- shot size;
- panel sử dụng.

Một camera mới không được tự tái thiết kế set.

### 3.5 Lighting map
Một scene có:
- key light;
- fill/ambient;
- hướng chính;
- nhiệt độ màu;
- thời điểm;
- vùng highlight;
- shadow logic.

Đổi camera không được đổi thời điểm/nguyên lý ánh sáng.

---

## 4. Perspective như họa sĩ nền

### 4.1 Bắt buộc xác định horizon
Horizon = eye level của camera. Mỗi panel phải biết:
- low eye level;
- seated eye level;
- standing eye level;
- high angle.

Không để bàn/ghế/cửa có horizon riêng.

### 4.2 Vanishing logic
- kiến trúc mặt phẳng song song phải hội tụ nhất quán;
- dãy bàn song song không tự uốn thành vòng cung;
- bậc thang phải tăng cao theo cùng một hệ;
- vật giống nhau ở xa phải nhỏ dần theo perspective, không nhỏ ngẫu nhiên.

### 4.3 Reverse shot
Khi camera quay gần 180°:
- world LEFT/RIGHT không đổi;
- screen LEFT/RIGHT có thể đảo;
- eyeline phải match;
- landmark phải chiếu đúng bên màn hình;
- không giữ nhân vật ở “bên đẹp” nếu làm sai world-space.

### 4.4 180-degree line
Với hội thoại/hành động, đặt một **action axis**. Mặc định camera ở cùng một phía trục để người đọc không mất phương hướng. Nếu buộc cross axis:
- phải có neutral shot / movement / establishing giúp tái định hướng;
- page spec phải ghi rõ.

### 4.5 30-degree change
Hai shot liên tiếp không nên gần như cùng góc/cỡ khung nếu không cố ý tạo nhịp tĩnh. Đổi đủ camera angle hoặc shot size để người đọc cảm thấy đây là shot mới, không phải “cùng portrait đổi tay”.

---

## 5. Character blocking trước khi vẽ đẹp

Mỗi nhân vật trong panel phải có:
- vị trí world-space;
- hướng thân;
- hướng đầu/mắt;
- line of action;
- trạng thái tay trái / tay phải;
- prop đang cầm / đặt ở đâu;
- chân đứng/ngồi trên mặt phẳng nào;
- silhouette có đọc được hay không.

### 5.1 Hands
Tay là action carrier. Trước render phải biết:
- tay nào làm hành động;
- tay kia ở đâu;
- có bị cụt/che vô lý không;
- prop có đổi tay không.

### 5.2 Props
Mỗi prop có:
- owner;
- world position;
- visibility theo panel;
- state.

Không để prop teleport chỉ vì camera đổi.

### 5.3 Clothing
Outfit được khóa theo scene. Fold/shadow có thể đổi; cấu trúc cổ áo, tay áo, cà vạt, dây ba lô, giày không đổi.

---

## 6. Crowd direction

Crowd không phải texture vô danh.

Tạo **crowd matrix** cho mỗi scene đông người:
- 4–8 archetype nền;
- giới tính trình bày;
- kiểu tóc;
- kính/không kính;
- vóc người;
- pose;
- row/seat.

Quy tắc:
- không đặt hai archetype giống nhau cạnh nhau;
- không clone mặt+tóc+pose;
- background character không tự tạo reaction beat;
- độ chi tiết giảm theo depth;
- crowd phải tuân hướng chung của scene.

---

## 7. Đạo diễn panel và nhịp Manhwa dạng Flipbook

### 7.1 Mỗi panel phải có một chức năng chính
Chọn một:
- ESTABLISH;
- ACTION;
- REACTION;
- INFORMATION;
- EMOTION;
- TRANSITION;
- REVEAL.

Nếu panel cố làm 3–4 việc ngang nhau, cần tách hoặc ưu tiên lại.

### 7.2 Shot vocabulary
- EWS/WS: không gian, scale, thiết lập;
- MS: hành động và tương tác;
- MCU/CU: biểu cảm, thoại quan trọng;
- ECU: chi tiết có ý nghĩa;
- OTS/reverse: hội thoại;
- insert: prop/chi tiết.

Không lạm dụng CU/portrait khiến page mất cảm giác không gian.

### 7.3 Visual hierarchy
Một page phải biết:
- panel chính;
- panel phụ;
- focal point từng panel;
- focal path toàn trang.

Diện tích panel theo **trọng lượng kể chuyện**, không chia đều theo thói quen.

### 7.4 Left-to-right flow
- ánh mắt, gesture, chuyển động nên hỗ trợ luồng trái→phải khi hợp lý;
- tránh nhân vật nhìn ra ngoài mép trang ở chỗ cần kéo mắt vào panel kế;
- cuối trang có thể hướng chuyển động/ánh mắt về lần lật tiếp theo.

### 7.5 Balloon reserve
Trước render:
- ước lượng lượng chữ;
- chừa negative space;
- không đặt vùng balloon lên mặt, tay hành động, prop quan trọng;
- balloon dài cần panel đủ diện tích.

Mặc định page có thoại nên chừa khoảng 15–25% vùng composition cho lettering tùy lượng chữ; đây là heuristic production, không phải tỷ lệ cứng.

---

## 8. Giá trị, màu và ánh sáng

Trước color render phải kiểm **value hierarchy**:
- focal point có contrast mạnh nhất;
- background giảm cạnh/chi tiết;
- crowd không cạnh tranh nhân vật chính;
- silhouette đọc được khi thu nhỏ.

Trong cùng scene:
- một key-light logic;
- shadow direction thống nhất;
- skin/material phản ứng khác nhau với ánh sáng nhưng không đổi base design;
- không “mỗi panel một filter”.

---

## 9. Quy trình 7 cổng trước khi full render

### GATE P1 — SOURCE LOCK
Đã biết source, character reference, outfit, geometry, lighting và text load.

### GATE P2 — SCENE MODEL
Có floor plan/spatial map + landmark register + camera map.

### GATE P3 — PAGE THUMBNAIL
Có layout, panel weight, reading flow, balloon reserve.

### GATE P4 — BLOCKING
Dùng box/mannequin/silhouette hoặc mô tả cấu trúc:
- camera;
- horizon;
- character position;
- action;
- prop;
- landmark visible/hidden.

Không cần mặt đẹp.

### GATE P5 — STRUCTURAL QA
Phải PASS:
- perspective;
- world-space;
- eyeline;
- pose;
- props;
- panel flow;
- negative space.

Nếu FAIL ở đây: **cấm full render**.

### GATE P6 — RENDER
Chỉ sau P5 mới render manhwa hoàn chỉnh.

### GATE P7 — ART QA
Kiểm identity, anatomy, hands, materials, lighting, crowd, continuity. Lỗi cục bộ sửa cục bộ.

Lettering là gate riêng sau khi artwork được người dùng duyệt.

---

## 10. Render contract cho AI

Trước mỗi lượt full-page image generation, prompt/spec phải chứa:
- PAGE ID;
- PRE-FLIGHT VERSION;
- reference roles;
- world axes;
- camera table;
- panel table;
- character blocking;
- prop states;
- background must-see / must-not-see;
- lighting;
- crowd rules;
- lettering reserve;
- failure conditions.

Nếu thiếu một mục có ảnh hưởng geometry/narrative, không full render.

---

## 11. Quy tắc giảm token/chi phí

1. Không full render để kiểm topology.
2. Không regenerate toàn page vì một bàn tay/prop nhỏ sai nếu structure đã đúng.
3. Nếu A1/A3 sai cùng một set: sửa scene model/camera map, không thêm mỹ từ vào prompt.
4. Tái sử dụng Set Bible và camera đã PASS.
5. Tái sử dụng crowd archetype, không tạo lại từ đầu mỗi page.
6. Một lỗi đã log phải trở thành negative constraint ở lượt sau.
7. Ba lần cùng loại lỗi = **pipeline failure**, dừng generation và sửa spec/reference, không tiếp tục roll ảnh.

---

## 12. Chuẩn “con mắt họa sĩ” trước khi duyệt

Một page chưa đủ chỉ vì “đẹp”. Phải trả lời ĐẠT cho:
- câu chuyện có đọc được không;
- mắt người đọc đi đúng hướng không;
- focal point có rõ không;
- camera có logic không;
- perspective có cùng world model không;
- pose có tự nhiên và truyền hành động không;
- tay/prop có đúng không;
- background có đúng set không;
- ánh sáng có cùng scene không;
- panel có đủ khác biệt về shot/nhịp không;
- lettering có chỗ thở không;
- page có đọc tốt ở thumbnail và full size không.

Một lỗi canon, topology, sai action hoặc sai speaker là blocker dù rendering đẹp.
