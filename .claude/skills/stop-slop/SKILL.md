---
name: stop-slop
description: Gọt văn bản bị "slop" — câu sáo rỗng, từ thừa, giọng văn kiểu AI — thành văn gọn, cụ thể, tự nhiên như người thật viết. Dùng cho cả tiếng Việt lẫn tiếng Anh. Dùng skill này bất cứ khi nào người dùng dán một đoạn văn (bài đăng, email, mô tả sản phẩm, báo cáo, caption, bài blog…) và muốn nó bớt sáo, bớt dài dòng, bớt "giống AI viết", tự nhiên hơn, hoặc nói "gọt lại", "viết lại cho gọn", "bỏ mấy câu sáo rỗng", "đọc như ChatGPT viết", "de-slop", "/stop-slop" — kể cả khi họ chỉ nói "sửa cho hay hơn" với một đoạn văn có nhiều câu chữ hoa mỹ trống rỗng.
---

# Stop Slop

Nhiệm vụ: nhận một đoạn văn và trả lại bản đã gọt — giữ nguyên ý, sự thật và giọng của người viết, nhưng bỏ hết phần "slop": những chữ chiếm chỗ mà không mang thông tin. Người đọc thật sẽ lướt qua hoặc mất niềm tin khi gặp kiểu văn này, nên gọt đi làm văn bản đáng tin và dễ đọc hơn.

**Ngôn ngữ:** bản đã gọt giữ đúng ngôn ngữ của văn bản gốc (tiếng Việt thì ra tiếng Việt, tiếng Anh thì ra tiếng Anh). Phần giải thích viết bằng tiếng Việt.

## Slop trông như thế nào

Nhận diện theo chức năng, không chỉ theo danh sách từ — câu nào bỏ đi mà người đọc không mất thông tin gì thì đó là slop.

**Mở bài và kết bài rỗng**
- VI: "Trong thời đại công nghệ 4.0 ngày nay…", "Có thể nói rằng…", "Không thể phủ nhận rằng…", "Tóm lại, có thể thấy…", "Hy vọng bài viết này hữu ích với bạn!"
- EN: "In today's fast-paced world…", "It's worth noting that…", "In conclusion…", "I hope this helps!"

**Từ hoa mỹ không đo được**
- VI: "vô cùng", "cực kỳ", "tuyệt vời", "đột phá", "hàng đầu", "đẳng cấp", "trải nghiệm tuyệt vời", "giải pháp toàn diện", "mang đến giá trị", "nâng tầm"
- EN: "delve", "leverage", "seamless", "robust", "cutting-edge", "game-changer", "unlock", "elevate", "tapestry", "testament to", "in the realm of"

**Cấu trúc kiểu AI**
- "Không chỉ… mà còn…" / "It's not just X, it's Y" dùng lặp lại.
- Liệt kê đúng 3 tính từ cho có nhịp ("nhanh chóng, tiện lợi và hiệu quả").
- Câu hỏi tu từ rồi tự trả lời ("Vậy tại sao điều này quan trọng? Bởi vì…").
- Rào đón thừa: "có thể", "phần nào", "dường như", "arguably", "potentially" chồng lên nhau.
- Gạch đầu dòng và chữ in đậm dày đặc cho một ý đơn giản; emoji trang trí ở mỗi dòng.
- Lạm dụng dấu gạch ngang dài (—) để nối mọi mệnh đề.

**Lặp ý**: nói một ý hai lần bằng hai cách, hoặc câu cuối đoạn tóm lại đúng câu đầu.

## Cách gọt

1. **Xác định ý cốt lõi** của từng đoạn: người viết thực sự muốn người đọc biết hoặc làm gì?
2. **Cắt** những câu không mang thông tin (mở bài rỗng, kết bài chúc tụng, câu tóm tắt lặp).
3. **Thay chữ chung chung bằng chi tiết có sẵn trong văn bản.** "Chất lượng vượt trội" → nếu văn bản có nói "bảo hành 5 năm" thì dùng chính chi tiết đó. Không bịa số liệu hay sự thật mới — nếu văn bản không có chi tiết, cứ bỏ tính từ, hoặc để chỗ trống `[con số cụ thể]` và nói rõ trong phần giải thích.
4. **Câu ngắn, động từ mạnh, chủ ngữ rõ.** Ưu tiên câu chủ động.
5. **Giữ giọng người viết.** Văn thân mật thì vẫn thân mật; văn trang trọng thì vẫn trang trọng. Đừng biến mọi thứ thành một kiểu văn khô cứng.
6. **Giữ định dạng phù hợp với mục đích.** Caption Facebook vẫn có thể có hashtag; email vẫn có lời chào. Chỉ bỏ định dạng thừa.
7. **Đọc lại bản gọt** và tự hỏi: còn câu nào bỏ đi được không? Có mất ý nào của bản gốc không?

Bản gọt thường ngắn hơn bản gốc 30–60%, nhưng đừng cắt cho đủ con số — mục tiêu là mỗi câu đều có lý do tồn tại.

## Định dạng trả lời

```
## Bản đã gọt

<văn bản đã gọt, đặt trong khối code để dễ sao chép>

## Đã bỏ / sửa gì
- <loại slop 1>: "<trích ngắn từ bản gốc>" → <đã bỏ hay thay bằng gì>
- ... (3–6 ý, gộp các lỗi cùng loại)

Độ dài: <số từ gốc> → <số từ mới> từ.
```

Nếu văn bản gốc đã gọn, nói thẳng như vậy và chỉ sửa vài chỗ nhỏ — đừng sửa cho có.

## Ví dụ

**Đầu vào:**
> Trong thời đại số hóa ngày nay, việc sở hữu một chiếc laptop chất lượng là vô cùng quan trọng. Laptop X không chỉ mang đến hiệu năng vượt trội mà còn sở hữu thiết kế sang trọng, đẳng cấp. Với pin 12 giờ và trọng lượng chỉ 1,2kg, đây chắc chắn là người bạn đồng hành tuyệt vời cho mọi hành trình. Hãy trải nghiệm ngay hôm nay!

**Đầu ra:**

````
## Bản đã gọt

```
Laptop X nặng 1,2kg, pin dùng được 12 giờ — đủ cho một ngày làm việc không cần sạc. Đặt mua hôm nay.
```

## Đã bỏ / sửa gì
- Mở bài rỗng: "Trong thời đại số hóa ngày nay…" → bỏ, không mang thông tin.
- Tính từ không đo được: "hiệu năng vượt trội", "sang trọng, đẳng cấp", "tuyệt vời" → bỏ; giữ lại chi tiết thật (1,2kg, 12 giờ) và nói rõ lợi ích.
- Cấu trúc "không chỉ… mà còn…" → bỏ.
- Lời kêu gọi chung chung "Hãy trải nghiệm ngay" → đổi thành hành động cụ thể. Nếu có link hoặc giá, nên thêm vào.

Độ dài: 64 → 21 từ.
````
