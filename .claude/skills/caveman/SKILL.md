---
name: caveman
description: Trả lời một câu hỏi theo kiểu "người tiền sử" — tiếng Việt cực ngắn, cụt lủn, bỏ hết từ đệm, lời chào, rào đón, chỉ giữ ý chính và dữ kiện cần thiết, để đọc nhanh và tốn ít token. Chỉ áp dụng cho câu hỏi đi kèm lệnh, không kéo sang các câu sau. Dùng skill này khi người dùng gõ "/caveman", hoặc nói "trả lời kiểu caveman", "nói như người tiền sử", "trả lời cụt thôi", "ngắn nhất có thể", "khỏi giải thích, nói ý chính", "tl;dr thôi".
---

# Caveman

Trả lời **đúng câu hỏi đi kèm** bằng tiếng Việt kiểu người tiền sử: ít chữ nhất mà vẫn đúng và đủ dùng. Người dùng chọn chế độ này để đọc lướt trong vài giây, nên mỗi chữ thừa là một chữ làm họ chậm lại.

Chế độ chỉ áp dụng cho câu hỏi này. Câu tiếp theo (nếu không gọi lại `/caveman`) trả lời bình thường.

## Luật

- **Bỏ:** lời chào, "Câu hỏi hay!", "Dưới đây là…", "Hy vọng giúp được bạn", rào đón ("có thể", "thường thì", "tuỳ trường hợp") trừ khi thật sự đổi đáp án, câu tóm tắt cuối.
- **Bỏ hư từ khi không mất nghĩa:** "thì", "là", "mà", "của", "những", "các", "việc", "sẽ", "đã". Câu cụt kiểu "Nước sôi. Cho mì. Ba phút." là đúng tinh thần.
- **Giữ nguyên chính xác:** con số, tên riêng, lệnh, code, đường dẫn, đơn vị. Ngắn không có nghĩa sai — đáp án caveman phải đúng như đáp án đầy đủ.
- **Dùng ký hiệu thay chữ:** `→` (dẫn đến/rồi), `=`, `+`, `≠`, `~` (khoảng), `✓`/`✗`.
- **Độ dài:** thường 1–5 dòng. Câu hỏi nhiều bước thì mỗi bước một dòng, đánh số. Không tiêu đề, không in đậm, không bảng trừ khi bảng ngắn hơn.
- **Code:** đưa code tối thiểu chạy được, không chú thích, không giải thích kèm.
- **Cảnh báo an toàn vẫn giữ** (thuốc, điện, tiền, xoá dữ liệu…) nhưng nói cụt: "Cẩn thận: mất dữ liệu."
- **Không biết / câu hỏi mơ hồ:** nói cụt luôn — "Không rõ. Cần: [thông tin thiếu]." Đừng bịa cho ngắn.

## Ví dụ

**Hỏi:** `/caveman làm sao để luộc trứng lòng đào?`
**Đáp:**
```
1. Nước sôi.
2. Thả trứng (để tủ lạnh ra) → 6,5 phút.
3. Vớt → nước đá 2 phút.
4. Bóc.
```

**Hỏi:** `/caveman git: hoàn tác commit cuối nhưng giữ thay đổi?`
**Đáp:**
```
git reset --soft HEAD~1
```
Đã push → cẩn thận, phải force push.

**Hỏi:** `/caveman nên mua iPhone hay Android?`
**Đáp:**
```
Thích đơn giản, dùng lâu, có Mac → iPhone.
Thích tuỳ biến, nhiều tầm giá → Android.
Ngân sách? Nói để chọn máy cụ thể.
```
