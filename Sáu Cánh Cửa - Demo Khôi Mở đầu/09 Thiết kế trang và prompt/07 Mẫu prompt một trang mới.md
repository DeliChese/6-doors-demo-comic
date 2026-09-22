# Mẫu spec một trang Manhwa — production

Điền theo `00 Pipeline tiền kỳ một trang Manhwa.md`. Không full-render nếu chưa PASS.

## 1. Story source
- PAGE ID:
- Nguồn:
- Beat toàn trang:
- Thứ tự đọc:

## 2. Reference roles
| Reference | Version | Vai trò | Được phép quyết định | Không được phép quyết định |
|---|---|---|---|---|
| … | … | CHARACTER / OUTFIT / GEOMETRY / LIGHTING / LAYOUT | … | … |

## 3. Scene Lock Card
- Time:
- FRONT:
- BACK:
- WORLD LEFT:
- WORLD RIGHT:
- Confirmed landmarks:
- Unknown zones:
- Character world positions:
- Prop world positions:
- Key-light direction:

## 4. Camera Table
| Panel | CAM-ID | Position | Look direction | Eye level | FOV | Shot size | Axis side |
|---|---|---|---|---|---|---|---|
| … | … | … | … | … | … | … | … |

## 5. Blocking Table
| Panel | Character | World position | Body | Eyeline | Left hand | Right hand | Props | Must-see BG | Must-not-see BG |
|---|---|---|---|---|---|---|---|---|---|
| … | … | … | … | … | … | … | … | … | … |

## 6. Panel direction
| Panel | Function | Narrative weight | Focal point | Motion/eyeline flow | Balloon reserve |
|---|---|---|---|---|---|
| … | ESTABLISH/ACTION/REACTION/... | main/sub | … | … | … |

## 7. Lighting / value
- Key light:
- Fill:
- Color temperature:
- Value focal:
- Background detail falloff:

## 8. Crowd
- Archetype count:
- Variation:
- Direction:
- Forbidden reaction:
- Depth simplification:

## 9. Negative constraints
Liệt kê lỗi đã từng gặp có nguy cơ lặp.

## 10. Preflight verdict
- [ ] PASS TO RENDER
- [ ] REVISE BLOCKING
- [ ] BLOCKED — NEED SOURCE/DECISION

Chỉ khi **PASS TO RENDER** mới viết prompt full-render.

## 11. Render contract
- Preflight version:
- Layout không được thay:
- Geometry không được thay:
- Character blocking không được thay:
- Chỉ được cải thiện rendering/anatomy/material/light trong phạm vi đã khóa.

## 12. Post-render QA
Phân loại lỗi: LOCAL / PANEL / SYSTEMIC. SYSTEMIC → quay lại preflight, không full reroll mù.
