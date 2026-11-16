# Concept — video 161s dọc (576x1024), voiceover tiếng Việt

## Concept đúng (preset MỚI: headline-dataviz)

Tech-storytelling 1 ý 1 beat: dòng kicker xám nhỏ + headline trắng lớn (2-4 dòng)
+ dashboard card tối màu chứa data-viz (bars, dot cascade, area chart, số %).
Không talking head, không footage. Nền đen xuyên suốt.

Khác kinetic-type: chữ chỉ là 1/3 khung, signature là card dashboard vẽ bằng code.
Khác pipeline-diagram: không có mũi tên/quy trình, mỗi card là 1 biểu đồ độc lập.

## Công cụ cần thiết (chỉ visual, bỏ voice)

- HyperFrames: khung dọc, kicker + headline động, card layout.
- SVG vẽ bằng code cho 4 loại chart: progress bars, dot cascade, vertical bars, area line.
  Figure phức tạp → animate skill (math style); đơn giản → SVG thuần.
- Timing: word/segment timestamps từ Whisper (đã có transcript 44 segments).
- Không cần: ComfyUI, whiteboard, footage người.

## Khung sườn kịch bản (từ transcript)

| Beat | Mốc | Nội dung | Visual |
|------|-----|----------|--------|
| Hook | 0–9s | 152 lỗi runtime, prompt suy thoái theo thời gian | Headline + card tổng quan |
| T1 | 17–28s | 126 cổng, 19 cổng browser, cấm selector rỗng | Progress bars 100% |
| T2 | 28–37s | Bơm 964 lỗi đối chứng âm | Dot cascade 16 nhóm |
| T3 | 37–41s | Cấm AI nới trần nợ kỹ thuật | Headline + lock card |
| T4 | 41–52s | 3 mã thoát: 1 cấm retry, 75 retry 1 lần | So sánh 2 nhánh |
| T5-6 | 52–65s | 839 test tỉnh, zombie, chấm chéo | Checklist/bars |
| Harness | 65–111s | Harness², ablation 5.3/3.7/1.5, 58.871 ký tự → skill | Area chart + bars |
| Scale | 111–134s | Đa máy 60s, 4 khoảng trống, cổng 4 bước | Sơ đồ vùng |
| Kết | 134–161s | 6 tầng + vòng lặp, trụ cột 5 Figma, chào | Tổng kết + CTA |

Tổng ~9 shot, mỗi shot 8–20s. Voice giữ nguyên của tác giả khi remake? Không —
theo quyết định bỏ voice: remake bản câm + sub, hoặc TTS sau (ngoài scope).
