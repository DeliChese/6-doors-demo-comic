# Pipeline tiền kỳ một trang Manhwa

File này là **cổng bắt buộc trước full render**. Không tạo page hoàn chỉnh trực tiếp từ kịch bản + prompt nếu chưa đi qua các bước dưới đây.

## Stage A — Story beat map

| Panel | Beat | Chức năng | Thông tin bắt buộc | Không được tự thêm |
|---|---|---|---|---|
| … | … | ESTABLISH/ACTION/REACTION/... | … | … |

Mỗi panel chỉ có một beat chính.

## Stage B — Scene lock card

- SCENE ID:
- Time:
- FRONT:
- BACK:
- WORLD LEFT:
- WORLD RIGHT:
- Confirmed landmarks:
- Unknown/unobserved zones:
- Character positions:
- Prop positions:
- Key light direction:
- Geometry anchor:
- Lighting anchor:

Nếu unknown ảnh hưởng trực tiếp action/camera, dừng và hỏi/đề xuất trước.

## Stage C — Camera table

| Panel | CAM-ID | Camera position | Look direction | Eye level | FOV class | Shot size | Axis side |
|---|---|---|---|---|---|---|---|
| … | … | … | … | … | … | … | … |

Kiểm reverse shot bằng world-space, không bằng “nhân vật bên phải/bên trái ảnh”.

## Stage D — Blocking table

| Panel | Character | World position | Body direction | Eyeline | Left hand | Right hand | Props | Must-see BG | Must-not-see BG |
|---|---|---|---|---|---|---|---|---|---|
| … | … | … | … | … | … | … | … | … | … |

## Stage E — Page thumbnail

Phải xác định:
- panel main/sub;
- width/height tương đối;
- gutter;
- focal point;
- visual flow;
- balloon reserve;
- page-turn intent nếu có.

Không cần render đẹp. Wireframe/SVG/text blueprint đủ.

## Stage F — Preflight verdict

Chỉ có ba trạng thái:
- **PASS TO RENDER**
- **REVISE BLOCKING**
- **BLOCKED — NEED SOURCE/DECISION**

Không dùng “có vẻ ổn”.

### PASS TO RENDER chỉ khi
- [ ] Beat đúng nguồn.
- [ ] Scene model không mâu thuẫn.
- [ ] Camera projection đúng.
- [ ] 180°/eyeline rõ.
- [ ] Perspective/horizon có logic.
- [ ] Character blocking đúng.
- [ ] Hands/props có state.
- [ ] Crowd direction rõ.
- [ ] Layout có hierarchy.
- [ ] Balloon reserve đủ.
- [ ] Lighting map thống nhất.
- [ ] Không có landmark bị tự bịa.

## Stage G — Render request

Full render phải ghi:
- Preflight ID/version đã PASS.
- Không được thay blocking/layout/geometry đã PASS chỉ để “đẹp hơn”.
- Nếu model không giữ được structure, output = FAIL; không sửa canon theo output.

## Stage H — Post-render QA

So output với preflight, không chỉ so với prompt.

Phân lỗi:
- LOCAL: mặt/tay/prop nhỏ → repair vùng/panel.
- PANEL: một panel sai camera/action → regenerate/sửa panel.
- SYSTEMIC: nhiều panel sai geometry/style/canon → quay về preflight, không full reroll mù.
