# Cài skill giao-viec-ai

Skill nhận việc: bạn giao một việc, AI hiểu ý bạn trước, chưa rõ thì hỏi lại những điều cơ bản và quan trọng nhất, rồi trình bản xác nhận gồm tên việc, mục tiêu, việc sẽ làm, đầu ra bàn giao, tiêu chuẩn đạt. Bạn đồng ý thì AI mới bắt tay làm.

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
4. Báo lại: đường dẫn đầy đủ của tệp vừa tạo, cách gọi skill, và nhắc tôi tắt hẳn công cụ rồi mở lại.

Tôi đồng ý cho bạn đọc mạng ở đúng đường dẫn trên và ghi đúng một tệp vào thư mục skill cá nhân của tôi.
```

AI hỏi xin phép đọc mạng, tạo thư mục hoặc ghi tệp thì bấm cho phép.

Dấu hiệu thành công: AI báo lại đường dẫn đầy đủ của tệp vừa cài, kết thúc bằng `giao-viec-ai/SKILL.md`, kèm câu lệnh gọi skill.

## Kho này có gì

| Tệp | Nội dung |
| --- | --- |
| `SKILL.md` | Bản hướng dẫn công việc cho AI, viết bằng chữ thường, 96 dòng |
| `HUONG-DAN-CAI.md` | Chính là tệp bạn đang đọc |

Không có tệp nào khác, không có thư mục con, không có mã chạy.

## Chạy thử

Tắt hẳn công cụ AI rồi mở lại. Gõ riêng dấu `/` (Claude) hoặc `$` (Codex) vào ô nhắn, thấy `giao-viec-ai` trong danh sách là công cụ đã nhận skill.

Gửi thử:

- Claude: `/giao-viec-ai viết lại yêu cầu này cho rõ: làm slide chuyên nghiệp hơn`
- Codex: `$giao-viec-ai viết lại yêu cầu này cho rõ: làm slide chuyên nghiệp hơn`

Dấu hiệu thành công: AI hỏi lại bạn những điều còn thiếu, hoặc trình bản xác nhận có đủ các mục Tên việc, Mục tiêu, Yêu cầu thực hiện, Đầu ra cần bàn giao, Tiêu chuẩn đạt, rồi dừng lại hỏi bạn có đồng ý để bắt đầu làm không.

## Lỗi hay gặp

1. **Không thấy skill trong danh sách.** Thoát hẳn công cụ AI rồi mở lại, đóng cửa sổ thôi là chưa đủ.
2. **Tệp nằm sai chỗ.** Hỏi AI: "Kiểm tra giúp tôi tệp SKILL.md của skill giao-viec-ai đang nằm ở đâu, có đúng thư mục skill cá nhân của công cụ này không." Sai chỗ thì nhờ AI chuyển sang đúng chỗ.
3. **Gõ nhầm ký hiệu.** Claude gọi skill bằng `/`, Codex gọi bằng `$`.
4. **AI làm luôn, không trình bản xác nhận.** Mở tệp `SKILL.md` xem dòng thứ hai có đúng `name: giao-viec-ai` không. Tệp bị sửa thì dán lại prompt ở mục Cách cài để cài lại.
5. **AI hỏi lại cho chắc trước khi tải.** Bình thường, nó đang xin phép. Trả lời đồng ý là nó làm tiếp.
