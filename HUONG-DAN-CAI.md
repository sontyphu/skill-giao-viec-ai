# Cài skill giao-viec-ai

## Skill này giúp gì khi bạn giao việc cho AI

Giao việc cho AI hay hỏng ở một chỗ: bạn nói một câu ngắn, AI tự đoán ý rồi làm luôn. Làm xong mới thấy lệch, bạn phải sửa đi sửa lại nhiều vòng.

Skill `giao-viec-ai` chặn đúng chỗ đó. Khi bạn gọi skill kèm một việc, AI làm ba điều trước khi bắt tay:

1. **Hiểu ý bạn.** Xác định việc gì, làm để đạt mục tiêu gì, cần giao ra cái gì, thế nào là đạt.
2. **Hỏi lại chỗ chưa rõ.** Chỉ hỏi những điều cơ bản, quan trọng nhất, mỗi câu một ý. Điều nhỏ không cần hỏi thì AI ghi thành giả định để bạn nhìn thấy.
3. **Trình bản xác nhận.** Gồm Tên việc, Mục tiêu, Yêu cầu thực hiện, Đầu ra cần bàn giao, Tiêu chuẩn đạt. AI dừng lại hỏi bạn có đồng ý không. Bạn đồng ý thì AI mới làm, muốn sửa thì AI sửa bản xác nhận và trình lại.

Tác dụng lớn nhất là biến yêu cầu mơ hồ thành tiêu chuẩn cụ thể. Bạn nói "làm slide chuyên nghiệp hơn", bản xác nhận sẽ ghi: rút gọn chữ, mỗi slide một thông điệp, đồng bộ màu, font và bố cục, thêm hình ảnh hoặc sơ đồ. Đọc bản xác nhận là bạn biết AI sẽ làm gì và giao ra cái gì, nên AI làm đúng ngay từ đầu, bớt sửa nhiều vòng.

Khi cần giao việc, gõ `/giao-viec-ai` (Claude) hoặc `$giao-viec-ai` (Codex) rồi viết tiếp việc bạn muốn giao.

## Cách cài

Mở công cụ AI của bạn, chép nguyên khối dưới đây, dán vào ô nhắn rồi gửi.

```
Cài giúp tôi một skill vào máy.

Nguồn: https://github.com/sontyphu/skill-giao-viec-ai
Đây là kho công khai, chỉ có 2 tệp văn bản là SKILL.md và HUONG-DAN-CAI.md. Không có mã chạy, không có script, không cài thêm phần mềm, không cần khoá hay mật khẩu, không gửi dữ liệu của tôi đi đâu.

Làm giúp tôi 4 việc theo đúng thứ tự:

1. Kiểm tra: tải https://raw.githubusercontent.com/sontyphu/skill-giao-viec-ai/main/SKILL.md rồi đọc hết.
2. Xác minh: xác nhận tệp chỉ là hướng dẫn bằng chữ, dòng đầu là ---, có name: giao-viec-ai và có phần mô tả. Nếu thấy mã chạy, lệnh hệ thống, đòi khoá hoặc yêu cầu gửi dữ liệu ra ngoài thì dừng lại, báo tôi, đừng cài.
3. Cài đặt: chép nguyên văn tệp vào thư mục skill cá nhân của chính bạn, giữ đúng tên. Claude Code: ~/.claude/skills/giao-viec-ai/SKILL.md. Codex: ~/.agents/skills/giao-viec-ai/SKILL.md. Không sửa một chữ nào. Thư mục chưa có thì tạo.
4. Báo lại: đường dẫn đầy đủ của tệp vừa tạo.

Tôi đồng ý cho bạn đọc mạng ở đúng đường dẫn trên và ghi đúng một tệp vào thư mục skill cá nhân của tôi.
```

AI hỏi xin phép đọc mạng, tạo thư mục hoặc ghi tệp thì bấm cho phép.

Dấu hiệu thành công: AI báo lại đường dẫn đầy đủ của tệp vừa cài, kết thúc bằng `giao-viec-ai/SKILL.md`.

## Kho này có gì

| Tệp | Nội dung |
| --- | --- |
| `SKILL.md` | Bản hướng dẫn công việc cho AI, viết bằng chữ thường, 96 dòng |
| `HUONG-DAN-CAI.md` | Chính là tệp bạn đang đọc |

Không có tệp nào khác, không có thư mục con, không có mã chạy.

## Kiểm tra công cụ đã nhận skill

- **Claude:** tắt hẳn app rồi mở lại (chuột phải biểu tượng Claude dưới khay đồng hồ, chọn Exit; máy Mac nhấn Command và Q). Gõ `/giao-viec` vào ô nhắn, chưa bấm gửi, thấy `giao-viec-ai` hiện ra là đã nhận.
- **Codex:** không cần tắt app. Gõ `$giao viec` vào ô nhắn, chưa bấm gửi, thấy Giao Viec Ai hiện ra là đã nhận.

## Lỗi hay gặp

1. **Claude không thấy skill trong danh sách.** Thoát hẳn app rồi mở lại, đóng cửa sổ thôi là chưa đủ.
2. **Tệp nằm sai chỗ.** Hỏi AI: "Kiểm tra giúp tôi tệp SKILL.md của skill giao-viec-ai đang nằm ở đâu, có đúng thư mục skill cá nhân của công cụ này không." Sai chỗ thì nhờ AI chuyển sang đúng chỗ.
3. **Gõ nhầm ký hiệu.** Claude gọi skill bằng `/`, Codex gọi bằng `$`.
4. **AI làm luôn, không trình bản xác nhận.** Mở tệp `SKILL.md` xem dòng thứ hai có đúng `name: giao-viec-ai` không. Tệp bị sửa thì dán lại prompt ở mục Cách cài để cài lại.
5. **AI hỏi lại cho chắc trước khi tải.** Bình thường, nó đang xin phép. Trả lời đồng ý là nó làm tiếp.
