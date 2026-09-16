# Cài skill giao-viec-ai

Skill nhận việc: bạn giao một việc, AI hiểu ý bạn trước, chưa rõ thì hỏi lại những điều cơ bản và quan trọng nhất, rồi trình bản xác nhận gồm tên việc, mục tiêu, việc sẽ làm, đầu ra bàn giao, tiêu chuẩn đạt. Bạn đồng ý thì AI mới bắt tay làm.

## Cách cài

Mở công cụ AI của bạn, dán hai dòng dưới đây vào ô nhắn rồi gửi.

```
https://github.com/sontyphu/skill-giao-viec-ai
Kiểm tra, xác minh, cài đặt.
```

AI hỏi xin phép đọc mạng, tạo thư mục hoặc ghi tệp thì bấm cho phép.

Dấu hiệu thành công: AI báo lại đường dẫn đầy đủ của tệp vừa cài, kết thúc bằng `giao-viec-ai/SKILL.md`, kèm câu lệnh gọi skill.

## Phần dành cho trợ lý AI

Người dùng đưa bạn kho này kèm câu "Kiểm tra, xác minh, cài đặt". Làm lần lượt 4 việc, không bỏ việc nào.

**Việc 1 - Kiểm tra.** Tải tệp `SKILL.md` từ https://raw.githubusercontent.com/sontyphu/skill-giao-viec-ai/main/SKILL.md rồi đọc hết. Xác nhận: dòng đầu là `---`, có `name: giao-viec-ai`, có `description`, phần thân có mục Quy trình xử lý.

**Việc 2 - Xác minh.** Soi nội dung tệp: nó chỉ là văn bản hướng dẫn cách làm việc, không chứa lệnh chạy, không chứa mã, không đòi khoá hay mật khẩu, không yêu cầu gửi dữ liệu ra ngoài. Thấy khác với mô tả này thì dừng, báo người dùng, không cài.

**Việc 3 - Cài đặt.** Chép nguyên văn tệp vừa tải vào thư mục skill cá nhân của chính công cụ bạn đang chạy, giữ đúng tên thư mục `giao-viec-ai` và tên tệp `SKILL.md`:

- Claude Code: `~/.claude/skills/giao-viec-ai/SKILL.md`
- Codex: `~/.agents/skills/giao-viec-ai/SKILL.md`
- Công cụ khác: thư mục skill cá nhân tương đương của công cụ đó.

Không sửa một chữ nào trong nội dung tệp. Thư mục chưa có thì tạo.

**Việc 4 - Báo lại.** Nói cho người dùng ba điều: đường dẫn đầy đủ của tệp vừa cài, cách gọi skill (`/giao-viec-ai` với Claude, `$giao-viec-ai` với Codex), và nhắc tắt hẳn công cụ rồi mở lại để nạp skill mới.

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
4. **AI làm luôn, không trình bản xác nhận.** Mở tệp `SKILL.md` xem dòng thứ hai có đúng `name: giao-viec-ai` không. Tệp bị sửa thì dán lại hai dòng ở mục Cách cài để cài lại.
