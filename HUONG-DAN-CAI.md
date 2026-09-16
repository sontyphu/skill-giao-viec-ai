# Hướng dẫn cài skill giao-viec-ai

Skill nhận việc: AI hiểu đúng ý bạn trước khi làm. Chưa rõ ý thì hỏi lại những điều cơ bản, quan trọng nhất. Trước khi làm, AI trình bản xác nhận gồm tên việc, mục tiêu, việc sẽ làm, đầu ra bàn giao, tiêu chuẩn đạt. Bạn đồng ý thì AI bắt đầu làm.

## Cài đặt

Mở công cụ AI của bạn, đúng thư mục làm việc. Chép đúng câu giao việc của công cụ bạn dùng, dán vào ô nhắn rồi gửi.

**Nếu bạn dùng Claude:**

```
Cài giúp tôi skill giao-viec-ai.
Tải tệp SKILL.md từ https://raw.githubusercontent.com/sontyphu/skill-giao-viec-ai/main/SKILL.md
Lưu vào thư mục skills cá nhân của Claude trên máy tôi, đúng đường dẫn .claude/skills/giao-viec-ai/SKILL.md trong thư mục người dùng.
Giữ nguyên nội dung tệp, không sửa chữ nào.
Làm xong báo tôi đường dẫn đầy đủ của tệp.
```

**Nếu bạn dùng Codex:**

```
Cài giúp tôi skill giao-viec-ai.
Tải tệp SKILL.md từ https://raw.githubusercontent.com/sontyphu/skill-giao-viec-ai/main/SKILL.md
Lưu vào thư mục skills cá nhân của Codex trên máy tôi, đúng đường dẫn .agents/skills/giao-viec-ai/SKILL.md trong thư mục người dùng.
Giữ nguyên nội dung tệp, không sửa chữ nào.
Làm xong báo tôi đường dẫn đầy đủ của tệp.
```

AI hỏi xin phép tải tệp, tạo thư mục hoặc ghi tệp thì bấm cho phép.

Dấu hiệu thành công: AI báo lại đường dẫn tệp, kết thúc bằng `giao-viec-ai\SKILL.md` (Mac: `giao-viec-ai/SKILL.md`).

## Chạy thử

Tắt hẳn công cụ AI rồi mở lại để nó nạp skill mới. Gõ riêng dấu `/` (Claude) hoặc `$` (Codex) vào ô nhắn, thấy `giao-viec-ai` trong danh sách là công cụ đã nhận skill.

Gửi thử:

- Claude: `/giao-viec-ai viết lại yêu cầu này cho rõ: làm slide chuyên nghiệp hơn`
- Codex: `$giao-viec-ai viết lại yêu cầu này cho rõ: làm slide chuyên nghiệp hơn`

Dấu hiệu thành công: AI hỏi lại bạn những điều còn thiếu, hoặc trình bản xác nhận có đủ các mục Tên việc, Mục tiêu, Yêu cầu thực hiện, Đầu ra cần bàn giao, Tiêu chuẩn đạt, rồi dừng lại hỏi bạn có đồng ý để bắt đầu làm không.

## Lỗi hay gặp

1. **Không thấy skill trong danh sách.** Thoát hẳn công cụ AI rồi mở lại, đóng cửa sổ thôi là chưa đủ.
2. **Tệp nằm sai chỗ.** Hỏi AI: "Kiểm tra giúp tôi tệp SKILL.md của skill giao-viec-ai đang nằm ở đâu, có đúng thư mục skills cá nhân của công cụ này không." Sai chỗ thì nhờ AI chuyển sang đúng chỗ.
3. **Gõ nhầm ký hiệu.** Claude gọi skill bằng `/`, Codex gọi bằng `$`.
4. **AI làm luôn, không trình bản xác nhận.** Mở tệp SKILL.md xem dòng thứ hai có đúng `name: giao-viec-ai` không. Tệp bị sửa thì dán lại câu giao việc ở mục Cài đặt để tải lại.
