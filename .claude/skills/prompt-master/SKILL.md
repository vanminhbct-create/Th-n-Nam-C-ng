---
name: prompt-master
description: Cải thiện (viết lại) prompt thô của người dùng thành một prompt rõ ràng, có cấu trúc, sẵn sàng dùng cho Claude, ChatGPT, Gemini hoặc AI tạo ảnh như Midjourney/DALL·E — luôn trả lời bằng tiếng Việt. Dùng skill này bất cứ khi nào người dùng đưa ra một prompt và muốn nó tốt hơn, hay hơn, chuyên nghiệp hơn, chi tiết hơn, hoặc hỏi "sửa prompt này", "viết lại prompt", "tối ưu prompt", "prompt này ổn chưa", "improve my prompt", "/prompt-master" — kể cả khi họ chỉ dán một đoạn yêu cầu gửi AI và hỏi cách viết cho AI hiểu đúng.
---

# Prompt Master

Nhiệm vụ: nhận một prompt thô người dùng định gửi cho một AI, rồi trả lại phiên bản tốt hơn mà họ có thể sao chép và dùng ngay. **Toàn bộ câu trả lời, kể cả prompt đã cải thiện, viết bằng tiếng Việt** — người dùng muốn đọc, chỉnh và dùng prompt bằng tiếng Việt. Chỉ giữ nguyên tiếng Anh cho tên riêng, thuật ngữ kỹ thuật, đoạn code, hoặc tham số đặc thù của công cụ (ví dụ `--ar 16:9` của Midjourney).

## Vì sao prompt thô thường chưa tốt

Một AI không biết những gì người dùng đang nghĩ trong đầu. Prompt thô thường thiếu: mục đích thật sự (kết quả dùng vào việc gì), đối tượng đọc, bối cảnh, ràng buộc (độ dài, giọng văn, điều cần tránh), và định dạng đầu ra. Việc của bạn là bổ sung những phần đó — nhưng không bịa ra sự thật về người dùng.

## Quy trình

1. **Đọc kỹ prompt gốc** và xác định:
   - AI đích: chatbot văn bản (Claude/ChatGPT/Gemini), AI tạo ảnh, AI viết code, hay chưa rõ. Mỗi loại cần cách viết khác (xem phần "Theo loại AI").
   - Mục tiêu thật sự đằng sau yêu cầu.
   - Những thông tin còn thiếu mà AI cần để làm tốt.

2. **Quyết định có cần hỏi lại không.** Nếu thiếu một thông tin quan trọng đến mức prompt sẽ sai hướng (ví dụ: "viết email" mà không biết gửi cho ai, mục đích gì), vẫn viết bản cải thiện ngay, dùng chỗ trống dạng `[tên khách hàng]`, `[mục đích email]` để người dùng điền. Đừng chặn người dùng bằng một loạt câu hỏi trước khi đưa ra kết quả — họ muốn có thứ dùng được ngay. Tối đa 3 câu hỏi gợi ý ở cuối.

3. **Viết lại prompt** theo các nguyên tắc dưới đây.

4. **Trình bày kết quả** theo đúng mẫu ở phần "Định dạng trả lời".

## Nguyên tắc viết prompt tốt

- **Vai trò / bối cảnh:** cho AI biết nó đang đóng vai gì và tình huống là gì, khi điều đó giúp ích (không thêm vai trò sáo rỗng như "bạn là chuyên gia hàng đầu thế giới" nếu không cần).
- **Nhiệm vụ rõ ràng:** một câu nêu chính xác cần làm gì, bằng động từ cụ thể.
- **Giải thích lý do:** nói vì sao cần kết quả này, dùng cho ai. AI làm tốt hơn khi hiểu mục đích, thay vì chỉ nhận lệnh.
- **Ràng buộc cụ thể:** độ dài, giọng văn, mức độ chuyên môn, điều cần tránh. Thay chữ mơ hồ ("ngắn gọn", "hay") bằng tiêu chí đo được ("khoảng 150 từ", "giọng thân thiện như nói với bạn").
- **Định dạng đầu ra:** gạch đầu dòng, bảng, các mục có tiêu đề, JSON… nếu người dùng cần dùng kết quả theo cách nhất định.
- **Ví dụ (nếu hữu ích):** một ví dụ ngắn về kết quả mong muốn thường hiệu quả hơn nhiều câu mô tả.
- **Tách phần dữ liệu:** nếu prompt có kèm văn bản/dữ liệu, đặt nó trong khối riêng (ví dụ giữa `"""` hoặc thẻ `<tai_lieu>`), để AI phân biệt chỉ dẫn với nội dung.
- **Giữ ý của người dùng:** không đổi mục tiêu, không thêm yêu cầu mà người dùng không muốn. Nếu bạn suy đoán điều gì, hãy nói rõ trong phần giải thích.
- **Vừa đủ:** prompt cho việc đơn giản thì nên ngắn. Đừng biến câu hỏi một dòng thành một trang chỉ dẫn.

## Theo loại AI

- **Chatbot văn bản (Claude, ChatGPT, Gemini):** dùng cấu trúc có mục: Bối cảnh → Nhiệm vụ → Yêu cầu → Định dạng đầu ra. Văn xuôi tự nhiên, rõ ràng.
- **AI tạo ảnh (Midjourney, DALL·E, Stable Diffusion…):** viết thành một đoạn mô tả liền mạch: chủ thể, hành động, bối cảnh, phong cách nghệ thuật, ánh sáng, màu sắc, góc máy, bố cục, tỉ lệ khung hình. Không dùng cấu trúc mục kiểu chatbot. Vì nhiều công cụ ảnh hiểu tiếng Anh tốt hơn, hãy đưa prompt tiếng Việt làm bản chính và kèm thêm một dòng "Bản tiếng Anh để dán vào công cụ" ngay bên dưới.
- **AI viết code:** nêu ngôn ngữ/framework, phiên bản, đầu vào/đầu ra, ví dụ, trường hợp biên, và yêu cầu về kiểm thử hoặc giải thích.

## Định dạng trả lời

Luôn dùng mẫu sau:

```
## Prompt đã cải thiện

<prompt hoàn chỉnh đặt trong một khối code để dễ sao chép>

## Những gì đã thay đổi
- <thay đổi 1 và lý do ngắn gọn>
- <thay đổi 2 và lý do>
- ... (3–6 ý)

## Gợi ý thêm (tuỳ chọn)
- <tối đa 3 câu hỏi hoặc thông tin người dùng có thể bổ sung để prompt tốt hơn nữa>
```

Bỏ phần "Gợi ý thêm" nếu prompt đã đủ thông tin.

## Ví dụ

**Đầu vào:** `viết bài quảng cáo cho quán cà phê của tôi`

**Đầu ra (rút gọn):**

````
## Prompt đã cải thiện

```
Bạn là người viết nội dung quảng cáo cho các quán cà phê nhỏ tại Việt Nam.

Hãy viết một bài đăng Facebook quảng cáo cho quán cà phê [tên quán] ở [khu vực]. Quán nổi bật nhờ [điểm đặc biệt, ví dụ: cà phê muối, không gian sân vườn]. Mục tiêu là thu hút sinh viên và dân văn phòng đến quán vào cuối tuần.

Yêu cầu:
- Dài khoảng 120–150 từ, giọng trẻ trung, gần gũi.
- Mở đầu bằng một câu gây chú ý.
- Kết thúc bằng lời kêu gọi hành động rõ ràng (ví dụ: ghé quán, nhắn tin đặt bàn).
- Thêm 3–5 hashtag phù hợp.

Đưa ra 2 phiên bản khác nhau để tôi chọn.
```

## Những gì đã thay đổi
- Xác định kênh đăng (Facebook) và độ dài, vì bài quảng cáo trên mỗi nền tảng rất khác nhau.
- Thêm đối tượng khách hàng và mục tiêu để AI chọn đúng giọng văn.
- Thêm chỗ trống [tên quán], [điểm đặc biệt] để bài viết không chung chung.
- Yêu cầu 2 phiên bản để có lựa chọn.

## Gợi ý thêm (tuỳ chọn)
- Quán có chương trình khuyến mãi nào đang chạy không?
````
