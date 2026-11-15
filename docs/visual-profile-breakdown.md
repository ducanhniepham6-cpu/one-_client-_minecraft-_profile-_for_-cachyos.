# Phân tích visual profile cho Bedwars 1.8.9

Bản này là phần mở rộng để giúp bạn xây dựng profile visual rõ ràng, không bị rối, không phát sinh lợi thế không công bằng. Mục tiêu là giữ trải nghiệm Bedwars dễ đọc, mượt và ổn định trên CachyOS.

## 1. HUD & scoreboard

### Mục tiêu
- Hiển thị trạng thái giỏi hơn mà không che map hoặc lối chơi
- Giữ HUD tối giản nhưng đủ thông tin cần thiết

### Thành phần cần ưu tiên
- health bar rõ dạng cao tương phản
- armor bar rõ ràng
- food / food bar nếu cần
- scoreboard dễ đọc
- timer hoặc cooldown hiển thị đúng vị trí

### Không nên làm
- Đặt quá nhiều text chồng lên nhau
- Thay đổi nội dung/độ lớn khiến bị che tầm nhìn chính
- Dùng mod chồng lặp cùng chức năng HUD

## 2. Crosshair & aim clarity

### Mục tiêu
- Crosshair dễ nhìn khi đánh PvP
- Không gây nằm cùng màu với nền
- Giữ cảm giác ổn với swing và hit timing

### Gợi ý
- Crosshair dạng sắc nét và có độ tương phản cao
- Tránh crosshair quá lớn hoặc có hiệu ứng khó đọc
- Dùng màu khác nếu background dùn quá nhiều màu

## 3. Nametag & entity visibility

### Mục tiêu
- Đọc được player trên map khi cận chiến
- Tăng khả năng nhìn mục tiêu, không phải lợi thế cheat

### Safe approach
- Thay đổi độ tương phản của tên, khung quét, màu nền
- Dùng chỉ biểu thị rõ dạng hiển thị cơ bản
- Không dùng overlay che kín player hay tự động phát hiện vị trí

## 4. Armor & item clarity

### Mục tiêu
- Dễ nhin armor, item trong tay, pickup item, cooldown, amount
- Nhanh nhận diện vật phẩm và tình trạng armor

### Gợi ý
- Hiển thị armor đầy đủ, rõ màu sắc
- Cập nhật item cooldown ở góc nhìn dễ đọc
- Không kích thước quá lớn, chỉ cần đủ để hiểu ngay

## 5. Performance & input smoothness

### Mục tiêu
- Mượt khi cận chiến, không lag khi đánh
- Không mất phản xạ trong những va chạm ngắn

### Khuyến nghị
- Giữ render distance ở mức 6 hoặc thấp hơn khi cần ổn định
- Giảm particles khi đang chơi PvP
- Giữ tối đa FPS vừa đủ để ổn định, không quá lạm dụng hiệu ứng đồ họa
- Tránh mod nặng, heavy animation, shader phức tạp

## 6. Keybind và flow

### Mục tiêu
- Tốc độ thao tác tốt hơn, không cần quá nhiều thao tác tay
- Tăng sự tiện lợi nhưng không phá luật server

### Safe approach
- Chỉ dùng keybind / quick action hữu ích
- Không dùng auto-click, auto-hit, auto-block
- Không sửa input để phát hiện player hoặc điều khiển ngoài logic game

## 7. Safe rule cho visual profile

Profile này chuẩn bị cho mục tiêu:
- rõ hình ảnh
- dễ đọc HUD
- ít xung đột mod
- tăng độ ổn định trong PvP

Nó KHÔNG bao gồm:
- auto clicker
- aim assist
- reach hack
- ESP / wallhack
- packet manipulation
- bypass anti-cheat

## 8. Profile khuyên dùng

### Clean Bedwars
- Vanilla 1.8.9 + OptiFine + 1 mod HUD tối thiểu
- Dành cho baseline và debug

### Visual Bedwars
- Thêm 1 hoặc 2 tính năng visual rõ, không chồng chéo
- Dành cho người chơi muốn rõ hơn nhưng vẫn giữ ổn định

### Tournament Safe
- Chỉ giữ phần tối thiểu, không dùng mod quá phức tạp
- Dành cho môi trường có kiểm tra chặt chẽ về server policy

## 9. Checklist cuối cùng

Trước khi dùng profile nào:
- xác nhận phiên bản 1.8.9
- xác định loader phù hợp
- xác định server có cho phép hay không
- xác minh từng mod từ nguồn chính thức
- test từng mod một cách độc lập
- chỉ giữ lại phần khiến hình hình rõ ràng mà không làm lợi thế không công bằng

Nếu cần, có thể tiếp tục xây thêm:
- `docs/bedwars-hud-layout.md`
- `docs/bedwars-performance-checklist.md`
- `docs/bedwars-quick-tune.md`
