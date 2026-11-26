# Cuộc thi mùa 3 – web học 21 ngày + trang quản trị (bản tách riêng)

Bản sao khung web học 21 ngày (`xem-truoc/`) và trang quản trị (`quan-tri/`), chép ngày 20/11/2026 để chạy mùa 3 mà **không ảnh hưởng trang chính**. Nội dung bài học mùa 3 lấy từ web lớp offline (mục dưới).

## Trạng thái truy cập hiện tại
- Không còn đăng ký/học thử, không thu số điện thoại; các buổi học trong 21 ngày đều mở sẵn.
- Hướng dẫn chỉ mở khi bấm nút **Hướng dẫn**, không tự bật hộp thoại khi vào trang.
- Trên iPhone/iPad, chọn **Chia sẻ → Thêm vào Màn hình chính** để mở như ứng dụng toàn màn hình.
- Hồ sơ tên bé chỉ để lưu tiến độ. Máy chủ mùa 3 chỉ cần thiết cho đồng bộ dữ liệu; không khóa quyền học.
- Các ghi chú tuyển sinh, học thử và kích hoạt ở phần dưới là lịch sử của hệ thống cũ, không áp dụng cho web học hiện tại.

- Web học mùa 3: ../cuoc-thi-mua-3
- Trang quản trị "Cuộc thi mùa 3": ./quan-tri
- Chế độ giáo viên: thêm `?gv=1`.

## Tách khỏi trang chính thế nào
| Phần | Trang chính | Mùa 3 |
|---|---|---|
| Code web | `xem-truoc/` | `cuoc-thi-mua-3/` (sửa ở đây không đổi trang chính, và ngược lại) |
| Trang quản trị | `quan-tri/` | `cuoc-thi-mua-3/quan-tri/` |
| Máy chủ + Sheet | `apps-script/Code.gs`, Sheet "Anh-Trung-Kids – Dữ liệu dự án" | `apps-script/cuoc-thi-mua-3/`, Sheet riêng mùa 3 (cách bật: `apps-script/cuoc-thi-mua-3/HUONG-DAN.md`) |
| Lưu trên máy của bé | khoá `lle-…` | khoá `lle3-…`: cùng một máy học cả hai bản không lẫn tiến độ, sao, avatar |
| Phiên đăng nhập quản trị | `qt-token` | `qt3-token` |
| Tranh, giọng | `xem-truoc/tai-nguyen/`, `xem-truoc/img/` | **dùng chung** (đọc từ `../xem-truoc/…`) để site không vượt giới hạn 1 GB của GitHub Pages |

Ba tệp nối lời với giọng (`canopy-audio-map.js`, `canopy-story-times.js`, `huong-dan.js`) được chép vào `tai-nguyen-chung/` vì chứa đường dẫn tương đối.
Vì tranh, giọng dùng chung: **đừng xoá hay đổi tên** file trong `xem-truoc/tai-nguyen/`; thêm tranh, giọng mới cho mùa 3 thì đặt trong `cuoc-thi-mua-3/` và trỏ tới đó.

## Việc còn lại trước khi mở mùa 3
1. Muốn đồng bộ tiến độ và điểm qua máy chủ, dán link `/exec` vào `SCORE_API` (`index.html`) và `API` (`quan-tri/index.html`). Khi chưa nối máy chủ, tiến độ vẫn lưu trên máy; quyền học 21 ngày không bị khóa.
2. Các ngày bắt đầu, học phí và nội dung tuyển sinh ghi ở nhật ký bên dưới chỉ để tham khảo lịch sử; không còn áp dụng cho luồng truy cập web học.

## Bài học mùa 3: lấy từ web lớp offline (20/11/2026)
- **Little Seed**: 18 ngày đầu của web Little Seed lớp offline (`../little-seed/`). **Canopy**: 18 ngày đầu của web Seedling 48 buổi (`../seedling/`).
- Khung 21 ngày giữ như mùa 2: buổi tự học 1–6, 8–13, 15–20 = ngày web lớp offline 1–18; ngày 7, 14, 21 là buổi Zoom (nội dung buổi Zoom trong `ol.js`, `OL_ZOOM`).
- Bấm vào một buổi: thanh tiêu đề của web mùa 3 + khung chạy bài của web lớp offline (`bai-ls/`, `bai-sd/`). Con chạm "Chạm để bắt đầu" một lần để bật tiếng.
- Mỗi bước xong +4 sao, xong buổi +10 sao, ghi ở tiến độ `seed-<i>.ol` / `canopy-<i>.ol`, gửi về Sheet mùa 3 như cũ (đổi quà, báo cáo dùng được).
- `bai-ls/`, `bai-sd/`: bản chép code của hai web lớp offline (không chép tranh, giọng), tắt máy chủ lớp offline, khoá lưu riêng từng bé (`m3ls-…`, `m3sd-…`). Sửa web lớp offline rồi muốn mùa 3 theo: chạy `python3 cuoc-thi-mua-3/cong-cu/dung_bai_offline.py` ở gốc repo. Đừng sửa tay `bai-ls/`, `bai-sd/`, `bai-offline.js`; sửa `cong-cu/nhung.js` (cầu nối bài ↔ web mùa 3) rồi chạy lại script.
- Nhiệm vụ quay clip: câu cho ba mẹ quay lấy từ tên bài song ngữ; phần "Hướng dẫn quay clip 2 cách" của mùa 2 đã bỏ vì thuộc bài cũ.
- Góc khám phá: Canopy dùng chung kho video của Little Seed (cùng chủ đề chào hỏi, tên tuổi, gia đình).
