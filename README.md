# Chat with stranger app

## Overview

Sử dụng app để chat với người lạ. Mỗi lần vào là ứng dụng tự động tìm __1__ người lạ để chat, nếu không thích có thể nhấn next.

Một số app tham khảo: [Azar](https://www.azar-web.com/#/home), [Chatvn](https://www.chatvn.me/)

## Yêu cầu

### Đăng ký

Người dùng đăng ký bằng `email` và `password`

Thêm thông tin cá nhân như:
- nickname
- avatar
- tuổi
- giới tính
- sở thích: list ra sẵn (`#football`, `#manga`, ...) để người dùng chọn
- vài dòng giới thiệu bản thân (optional)

### Thuật toán tìm người lạ

Thuật toán tìm người lạ là ngẫu nhiên theo filter sở thích, độ tuổi và giới tính

### Trong khi chat

Chat 1-1, có thể thấy được username + avatar + giới thiệu bản thân của nhau.

Gửi được tin nhắn text, hỗ trợ thêm gửi ảnh, file, ... cho nhau

Có thể next nếu cảm thấy nói chuyện không hợp

Sau khi chọn next hoặc người còn lại chọn next, app tự động tìm người lạ khác để tiếp tục chat

Nội dung chat cũ sẽ bị huỷ

## [Timeline](timeline.md)

## Diagram

### Activity diagram

[Sign in](diagram/activity/sign_in.md)

[Sign up](diagram/activity/sign_up.md)

[Chat](diagram/activity/chat.md)

### Sequence diagram

[Chat](diagram/sequence/chat.md)

### Database diagram

[Database](diagram/database/database.md)

### Class diagram

[Class](diagram/class/class.md)

### Architecture diagram

[Architecture](diagram/architecture/architecture.md)