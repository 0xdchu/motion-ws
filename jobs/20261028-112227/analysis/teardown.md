# Teardown — "152 lỗi runtime, 6 tầng kiểm soát" (headline + dashboard card, 163s, 9:16)

Nguồn: file local `/tmp/td_new/ref.mp4` (không có URL), ingest 2026-10-28, 576x1024, 163.03s, 30fps, có audio AAC.
Voice: nam Việt, 44 segments (audio.json, Whisper). Tác giả tự giới thiệu "Giang, Principal Product Engineer"; chủ đề là trụ cột 4 của hệ thống kiểm soát chất lượng AI (126 cổng CI, 6 tầng độ cứng, harness²). Không chép asset gốc vào repo.
Teardown này bổ sung `shots.md` (concept ban đầu) bằng số liệu mốc nối đo từ video; preset gợi ý: **headline-dataviz** (preset mới, xem `shots.md`).

## 1. Shots

Bố cục chung mọi shot: nền đen, trên cùng 2 dòng header xám cực nhỏ (tên trụ cột + "Hội 1 · 152 lỗi runtime…"), kicker xám nhỏ, headline trắng 2–4 dòng căn trái ở nửa trên, card dashboard tối bo góc ở nửa dưới (~y 440–1000 trên khung 1024).
Headline là **sub chạy theo voice**: từng từ hiện dần từ mờ (blur) → rõ, từ nhấn chuyển đỏ/xanh ("lỗi", "lỗi sản phẩm", ✓ xanh cuối câu).

| # | Mốc (s) | Loại shot | Bố cục (layers) | Chuyển động | Âm thanh/sub |
|---|---------|-----------|-----------------|-------------|--------------|
| 1 | 0–17 | Hook, chưa có card | Header xám + "Yo anh em!" mờ → "Mình là **Giang.** / Principal Product Engineer" → "một trăm năm mươi hai **lỗi** runtime thực tế trong tám ngày cao điểm." (từ "lỗi" đỏ) → "nhưng lời dặn trong prompt luôn suy thoái theo thời gian ✓" | Chữ blur-in từng từ; card nền xuất hiện ở ~0.2s | Voice 0–15.6s; câu hỏi chốt: lời dặn trong prompt phai theo thời gian |
| 2 | 17–41.5 | Card "126 Automated CI Gates Across 5 Verification Stages" | Badge xanh "126 CI gates", 4 hàng thanh sọc dọc (Stage 1-2 schema/types/ontology, Stage 3 dual-layer spec & VI gate, Stage 4 storybook & RPT grid audit, Stage 5 negative control & grader), mỗi hàng ~100 vạch + nhãn "100%" xanh; footer "Ballot tally · 100% mechanical enforcement" | Vạch xanh chạy đầy; vòng tròn highlight nhỏ chạy dọc theo hàng; số góc phải đổi "126 CI GATES" → "5 STAGES" (~20s) | Voice: 126 cổng / 6 tầng / tầng 1 mẫu số độ phủ 19 cổng browser / cấm selector rỗng / **tầng 2 bơm 964 lỗi / tầng 3** — card **không đổi** theo voice, vẫn ở 126 cổng |
| 3 | 41.5–88.8 | Card "964 Injected Negative-Control Faults Across 16 Bug Classes" | Badge đỏ "RED TEST", dot cascade chéo: 16 cột chấm tăng dần từ trái-dưới lên phải-trên (1,2,3…21 ở cột cuối), chấm trắng → hồng/đỏ ở cột cao; trục nghiêng, footer đổi "Gate Skepticism" → "Negative Control Injection" (~65.8s) | Chấm hiện từng cột trái→phải; số góc "RED TEST" → "964 SEEDED BUGS" | Voice: tầng 4 exit code 1 vs 75, tầng 5-6 (839 test, zombie, chấm chéo), rồi sang harness² (65.9s) |
| 4 | 88.8–134 | Card "Generator vs Independent Grader: Catching Subtle UX Bugs" | Badge "SEPARATE"; 5 cột thanh sọc (Token audit, Grid spt, AC match, Blind spot, UX rubric) đỉnh 100%/99%/100%/<1%/98%, số góc đổi "SEPARATE" → "0 SELF-MARK" | Cột lớn dần theo hàng, vòng tròn highlight quét; điểm "<1%" đỏ ở Blind spot là chỗ nhấn | Voice: ablation Google (gỡ skill −5,3; kịch bản −3,7; system prompt −1,5), 58.871 ký tự → skill, đa máy 60s, 4 khoảng trống, vùng cô lập, cổng 4 bước, mô hình chấm ≠ mô hình biên tập |
| 5 | 134–163 | Card "Google Research Harness²: Crystallizing Bugs into Reusable Skills" | Badge xanh "HARNESS²", area chart đường vạch đứng (bug caught → rule extracted → skill locked), đỉnh nhấn xanh "Skill Crystallized" | Đường area vẽ từ trái sang phải; đỉnh dựng thẳng đứng xanh | Voice: cầu nối Max Studio, 7 chống lộ điểm chấm, thí nghiệm 4 nhánh khóa chi phí; chốt 6 tầng + vòng lặp, trụ cột 5 (đọc bình luận designer trên Figma), chào "Tôi là Giang. Hẹn gặp lại anh em." |

Ghi chú: 5 card thực tế (không phải 9 shot như phỏng đoán ở `shots.md`); `shots.md` bảng khung sườn theo ý voice vẫn đúng cho nội dung, còn nhịp hình ảnh là 5 card.

## 2. Transition (bắt buộc, không bỏ qua)

Đo bằng scene-detect trên vùng card (fps 4): các mốc đổi card **0.2s, 41.5s, 65.8s (đổi footer, card giữ), 88.8s, 134.0s**.

- 0.2s: không có → card 126 gates hiện (fade/scale nhẹ ngay sau khung đầu). Frame đầu chỉ có header + chữ mờ, card vào sau 0.2s.
- 41.5s: card 126 gates → card 964 dot cascade: **hard-cut** (1 frame), rơi vào từ "Ở tầng bốn" (voice 41.7s). Voice nói 964 từ 27.9s nhưng card 964 đến sau 14s: hình trễ hơn voice ở đoạn này.
- 65.8s: footer card 964 đổi (Gate Skepticism → Negative Control Injection), card giữ; trùng "Để hệ thống không chỉ cứng vững…" (65.9s).
- 88.8s: 964 → grader bars: hard-cut, rơi vào "Trong phép thử loại bỏ…" (88.9s).
- 134.0s: grader → area chart harness²: hard-cut, rơi vào "Trên Max Studio…" (134.1s).
- Mọi mốc nối khớp mốc đầu câu voice trong ±0.3s, trừ chỗ 964 lệch ~14s so với lúc voice nhắc.
- Chữ headline: mỗi câu voice = 1 headline mới; câu cũ biến mất trước khi câu mới blur-in, không để khung trống quá ~1s (xem các tile trống ở 0.6–1.6s và 15.6–17.3s: sub chỉ còn header xám).

## 3. Spatial map

Không phải continuous-canvas: màn hình đơn, bố cục cố định (header / headline / card), không camera move. Bỏ qua.

## 4. Design system trích ra

- Nền đen #000, chữ trắng, kicker/header xám ~#888, nhấn đỏ (#ff3b4a gần đúng) cho "lỗi/RED TEST", nhấn xanh lá (#2bd96b gần đúng) cho "100%/PASS/SEPARATE/HARNESS²". Hai màu nhấn ↔ hai nghĩa: đỏ = lỗi/test bắt lỗi, xanh = cổng pass / hệ thống tốt.
- Card dashboard: nền #0c0c0c bo ~16px, viền mảnh, badge nhỏ trên-trái (bo tròn, xanh hoặc đỏ), tiêu đề card tiếng Anh trắng ~14px, subtitle xám, footer 2 dòng xám cực nhỏ, **số lớn góc trên-phải** đổi theo nhịp voice (126 → 5 STAGES → RED TEST → 964 → SEPARATE → 0 → HARNESS²).
- 4 loại chart vẽ bằng code (SVG đủ): thanh sọc ngang (progress), dot cascade chéo, cột thanh sọc đứng (so sánh), area đường vạch đứng.
- Chữ tiếng Việt viết số bằng chữ ("một trăm năm mươi hai", "hai mươi sáu", "sáu mươi giây") — sub là transcript đọc theo voice chứ không phải số; card tiếng Anh giữ số ("126", "964").
- Nhịp: 163s / 5 card, card dài nhất 47s (964), headline đổi mỗi 2–4s theo câu voice. Là template "1 ý 1 câu, headline blur-in + 1 card đổi mỗi ~30–45s".
- Đưa vào dataset/preset: `headline-dataviz` (nếu duyệt tách preset — đây là clip thứ 1; luật tách cần lặp lại lần 2 theo `presets/README.md`).

## 5. Câu hỏi mở

- Đưa vào preset mới `headline-dataviz` ngay hay chờ clip thứ 2 cùng kiểu (luật "tách preset mới nếu lặp lại lần 2")?
- Remake giữ card tiếng Anh (như gốc) hay Việt hoá hết?
- Giữ đúng số liệu của tác giả (126 cổng, 964 lỗi, 839 test, 58.871 ký tự) hay thay bằng số của chủ kênh? Đây là nội dung riêng của người khác — khi remake nên dùng số/dữ liệu của mình.
- Voice: bỏ (bản câm + sub) theo `shots.md`, hay TTS sau (ngoài scope)? Nhạc nền/SFX: chưa tách stem để kiểm tra (file audio chỉ transcript).
- Có cần đồng bộ card theo voice (card 964 vào lúc voice nhắc ở 27.9s) hay giữ lệch như gốc?
