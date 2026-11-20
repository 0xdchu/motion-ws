# Teardown — "chase_ai: Claude now does videos" (tutorial talking-head + screen-rec, 850s, 16:9)

Nguồn: file local `/tmp/ref_chase_ai.mp4` (job.file, kênh Chase AI), ingest 2026-10-27,
1280x720 30fps, 849.5s. Voice: nam Anh, 329 segments (`audio.json`, Whisper `small`,
CPU, `language=en`, chạy 2026-11-15). Lưu ý transcript: 6:35–6:42 Whisper lặp
"go ahead and go ahead..." (ảo giác, bỏ qua); "FFM peg" = FFmpeg, "obis 5.5" = Opus 5.5,
"skillery.dev" = skillsly/skills site đọc theo hình. Không chép asset gốc vào repo
(source.mp4 / frames / contact-sheet đã gitignore).

**Phân loại preset:** cả video KHÔNG khớp 1 preset. Khung ngoài là tutorial (webcam tròn
góc phải dưới + màn hình/clip nhúng). Cái đáng distill là các **clip demo nhúng**
(mục 1, shot D1–D5): D3 = pipeline-diagram (khớp preset đã gán), D1/D2 = motion-graphic
mẫu 3B1B / chữ động. Job giữ `preset: pipeline-diagram` cho phần D3; xem mục 5.

## 1. Shots

Lớp cố định mọi shot: webcam tròn ~270px góc phải dưới (có viền mờ), nền tối #0e0e10–#18191e.

| # | Mốc | Loại shot | Bố cục (layers) | Chuyển động | Âm thanh/sub |
|---|-----|-----------|-----------------|-------------|--------------|
| 1 | 0:00–0:08 | Cold open: reel demo | Clip nhúng toàn khung: chữ "EASE / SNAP / STRETCH / OVERSHOOT" nền kem + đồ thị easing; rồi ảnh côn trùng vẽ tay trên nền cam | Chữ kinetic trượt/giãn, đồ thị vẽ dần | VO: "You don't need Remotion / After Effects", không sub rời |
| 2 | 0:08–0:35 | Hook + lời hứa | Webcam to + (xen) clip demo; 4 ý: prompt, reference, skill | Hard-cut theo câu | VO giới thiệu 4 level |
| 3 | 0:36–1:50 | **D1 "A video is a function"** (clip 3B1B-style, one-shot) | Màn Claude Code (chat tối) → clip phóng toàn khung: `frame(t) =` + vòng tròn đơn vị + sóng sin θ hồng, khung viền vàng, lưới mờ; t đếm (3.54, 7.54) | Điểm vàng chạy vòng, đường sin vẽ dần (stroke draw), t tăng | VO đọc script clip: "Give it a time t, it returns one picture" |
| 4 | 1:10–1:20 | D2 so sánh | 2 khung vàng cạnh nhau `frame(6.95) = frame(6.95)` (cùng t, cùng ảnh) | Hai khung giống hệt, dấu = ở giữa | "Same t, same picture every time" |
| 5 | 1:20–1:48 | **D3 pipeline** (khớp preset) | `function frame(t){...}` code xanh → headless browser (khung có chấm 3 màu) → stack frames (= 123 / 240) → FFmpeg → ô play vàng; dưới là sóng `sound(t)` đỏ cam | Node hiện trái→phải, mũi tên nối, số frames đếm | "headless browser draws each frame, FFmpeg stitches" |
| 6 | 1:50–3:00 | Giải thích lại trên Excalidraw | Cùng sơ đồ D3 mở trong Excalidraw (toolbar tím bên trái), thêm ghi chú viết tay hồng: "javascript", vòng + mũi tên đỏ quanh headless browser / frames / FFmpeg / ô play; thanh timeline "60 samples per second" | Người vẽ chú thích tay đè lên sơ đồ, vòng khoanh theo lời | Giải thích 60 frames/s, Playwright |
| 7 | 3:00–3:36 | Mở level / ghi chú | Màn chat Claude Code (văn bản dài) | Tĩnh, cuộn nhẹ | VO nói 4 level |
| 8 | 3:36–4:07 | Sponsor (tự quảng cáo) | Trang Skool "Chase AI": thẻ Start Here, Claude Code Masterclass, Codex, Agency Protocol 01/02/03 | Tĩnh | Chat "Chase AI Plus" |
| 9 | 4:07–5:00 | Level 1: prompt + effort | Chat Claude Code: prompt "make a dynamic 15 second motion graphics video..." + kết quả; chạy low/high/ultra | Tĩnh, text cuộn | So low 20', high 30', ultra 8h |
| 10 | 5:00–5:40 | Demo kết quả low/high/ultra | Clip nhúng toàn khung: chữ "MAKE" nền cam, đối tượng 3D trên bục (cầu kính, khối) | Chuyển động suy từ 1 frame (camera/xoay chưa xác nhận) | So sánh 3 phiên bản low/high/ultra |
| 11 | 5:40–7:20 | Level 1b: storyboard | Chat + panel "A video is a function: storyboard" (46.45s, 1920x1080, 120 BPM, 7 beats, thumbs up/down theo panel) lưới thumbnail 4+3 | Panel zoom: từ chat → phóng ra lưới 7 ô → cuộn | "ask for a storyboard first" |
| 12 | 7:20–9:40 | Level 2: prompt structure | Excalidraw "Level 2: the tools and a loop": hộp prompt kem tô màu (độ dài, 16:9, JavaScript, soundtrack, Playwright + FFmpeg, contact sheet) + 4 ô xanh lá bên phải | Highlighter chạy theo lời; zoom sâu vào từng dòng (zoom ~3–4x), khoanh hồng | Liệt kê: length/aspect/JS/soundtrack/MP4/contact sheet |
| 13 | 9:40–10:00 | ElevenLabs | Trang web elevenlabs.io "Bringing technology to life" nền trắng | Tĩnh | Nhắc ElevenLabs MCP |
| 14 | 10:00–10:20 | Level 3: nơi tìm reference | Trang skillsly "Browse 475 Opus 5.5 videos" lưới thumbnail tối | Cuộn | "skillsly.dev" |
| 15 | 10:20–11:00 | **D4 Reference → recreate** | Clip nhúng 2 cột: tờ giấy cổ "9000 BC / 1844 / 221 BC / 1969" (tiền tệ → điện) | Trượt cân bằng, đếm năm | "composition close, content different" |
| 16 | 11:00–11:40 | Nguồn cảm hứng | Skillsly "Viral Opus 5.5 videos, with their prompts" + GitHub README Animate skill | Cuộn trang | nhắc Kevin trên Twitter |
| 17 | 11:40–13:30 | Level 4: skill Animate | GitHub README "Animate — procedural animation in any style, for Claude Code": thẻ 7 style (cut-paper, crosshatch, riso, sketchbook, isometric, ? your look); bảng "How it works" 0–5 (Intake…Delivery); Install | Cuộn README | Giải thích intake → storyboard → build → delivery |
| 18 | 13:30–14:10 | Outro demo + CTA | Clip nhúng tên lửa nét bút chì xanh trời (D5 phong cách sketchbook/crayon) | Tên lửa bay, mây trôi | CTA "Chase AI Plus" |

## 2. Transition

- Phần lớn là **hard-cut** (tutorial): chat → clip nhúng → chat, 0 frame đen, rơi đúng đầu câu VO.
- Chat → clip nhúng: **zoom/crop** vào vùng khung clip (shot 3: 0:36–1:00, chat thu nhỏ rồi clip chiếm toàn khung), không fade.
- Excalidraw: **camera-move liên tục** (pan + zoom trên 1 canvas), webcam tròn không đổi chỗ → neo mắt.
- Chỗ nối dễ lộ lỗi khi remake: 1:48→1:50 (sơ đồ D3 → cùng sơ đồ trong Excalidraw, cần khớp bố cục từng node) và 7:20→9:40 (zoom sâu chữ nhỏ trên canvas — mục 3).

## 3. Spatial map (phần Excalidraw, shot 6 và 12 — mini continuous-canvas)

- Shot 6: sơ đồ D3 nằm giữa canvas; ghi chú viết tay hồng chồng lên (javascript trên cùng, timeline "60 samples per second" ở dưới). Zoom 1x → ~1.5x, giữ node "headless browser" làm vật tham chiếu.
- Shot 12: 1 hộp prompt trái (≈60% rộng) + 4 ô ghi chú xanh phải. Camera đi 1x (toàn cảnh) → ~4x (từng dòng prompt, chữ nhỏ nhất toàn cảnh ≈ 10–11px ở 720p; zoom sâu ≈ 40px) → quay lại 1x. Có chỗ dừng lưng chừng > 0.5s khi ghi chú (vi phạm checklist continuous-canvas nếu remake y nguyên — nên dừng ở mức zoom cố định).

## 4. Design system trích ra

- **Nền:** #0e0e10 (UI/trang), #18191e (nền clip nhúng), chữ trắng #f2f2f2; khung viền vàng #e8c547 (khớp màu preset pipeline-diagram).
- **Nhấn:** hồng/magenta #d63fbf (đường sin/ghi chú), vàng điểm sáng #f5c542, xanh lá mềm (code, chữ `frame`), xanh lam (giá trị `t`), đỏ cam (sóng sound).
- **Chữ:** serif (frame(t), sinθ — kiểu 3B1B), mono cho code, viết tay hồng cho chú thích Excalidraw.
- **Cấu trúc tutorial tái dùng:** cold open demo → lời hứa "you don't need X" → 4 level (prompt → loop tự kiểm → reference → codify thành skill) → sponsor chen giữa (3:36–4:07) → CTA.
- **Mẫu pipeline-diagram từ D3:** 5 node (code → headless browser → frames → FFmpeg → play) + sóng âm song song phía dưới; khung vàng cho "browser/frames", nút play vàng ở cuối — bổ sung vào `presets/pipeline-diagram` một biến `PARALLEL_TRACK` (sóng sound(t)) nếu duyệt.
- **Webcam tròn** góc phải dưới ~270px, không che nội dung quan trọng (clip nhúng chừa vùng đó).
- **Nhịp:** 1 ý ≈ 8–25s tutorial; clip nhúng demo 10–50s; sơ đồ node 0.8–1.2s/node (khớp preset).

## 5. Câu hỏi mở

- Phạm vi remake: chỉ dựng lại D3 (pipeline-diagram, ~30s) hay cả D1+D2+D3 (clip "A video is a function" 46s)? Mặc định đề xuất: D3 trước, vì khớp preset.
- Video là tutorial dài 14 phút có webcam — preset `pipeline-diagram` chỉ áp cho 1 phần. Có tách preset "screen-tutorial" khi lặp lại lần 2 không (luật matching số 7)?
- Webcam tròn và các clip nhúng của người khác: remake dùng placeholder hay bỏ; chỉ học bố cục/nhịp, không chép nội dung.
- Whisper chạy `small` trên CPU (GPU driver lỗi tại thời điểm chạy); tên riêng (skillsly, Kevin) chưa kiểm chéo, đọc từ hình.
