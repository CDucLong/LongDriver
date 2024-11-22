"# LDriver" 
LDriver - Hướng Dẫn Vận Hành Xe Hai Bánh Tự Cân Bằng
"# Yêu cầu" 
Chuẩn bị phần cứng
Cài đặt phần mềm
Quy trình vận hành
Kiểm thử từng chức năng
Xử lý sự cố thường gặp
#1. Chuẩn bị phần cứng
Arduino Uno/Mega
MPU6050 (Cảm biến góc nghiêng)
#2 động cơ DC + Driver L298N
Module điều khiển từ xa (RF24L01)
Pin và mạch nguồn
Khung xe hai bánh
#Kết nối phần cứng:
#MPU6050:
VCC -> 5V
GND -> GND
SDA -> A4
SCL -> A5
#L298N & động cơ:
ENA -> Pin 5
IN1 -> Pin 6
IN2 -> Pin 7
IN3 -> Pin 8
IN4 -> Pin 9
ENB -> Pin 10
#2. Cài đặt phần mềm
Cài đặt Arduino IDE
Cài đặt các thư viện:
Wire.h
MPU6050.h
RF24.h
Tải code từ repository và nạp vào Arduino
#3. Quy trình vận hành
Kiểm tra kết nối phần cứng
Cấp nguồn cho hệ thống
Đặt xe ở vị trí thẳng đứng
Chờ 3-5 giây để cảm biến ổn định
Xe sẽ tự động bắt đầu cân bằng
#4. Kiểm thử từng chức năng
#4.1 Kiểm tra cảm biến góc nghiêng
Mở Serial Monitor (9600 baud)
Đặt xe thẳng đứng -> góc ≈ 0°
Nghiêng nhẹ xe -> kiểm tra góc hiển thị
#4.2 Kiểm tra cân bằng tự động
Đặt xe thẳng đứng
Xe sẽ tự động điều chỉnh:
Nghiêng trái -> động cơ trái tăng tốc
Nghiêng phải -> động cơ phải tăng tốc
#4.3 Kiểm tra điều khiển từ xa
Bật remote control
Kiểm tra các lệnh:
Di chuyển tiến/lùi
Rẽ trái/phải
Dừng
#5. Xử lý sự cố thường gặp
Xe không tự cân bằng
Kiểm tra kết nối MPU6050
Kiểm tra điện áp pin
Hiệu chỉnh lại các thông số PID
Xe rung lắc nhiều
Giảm giá trị Kp trong PID
Tăng giá trị Kd
Kiểm tra độ chắc chắn của khung xe
Điều khiển từ xa không hoạt động
Kiểm tra kết nối RF24L01
Kiểm tra địa chỉ kênh truyền
Kiểm tra pin remote
#Lưu ý quan trọng
Luôn đặt xe thẳng đứng khi khởi động
Duy trì điện áp pin ổn định
Kiểm tra độ chặt của các kết nối
Hiệu chỉnh PID dựa trên khối lượng thực tế
