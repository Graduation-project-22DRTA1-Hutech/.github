# ROS2-DIFF-DRIVE-CONTROLLER 🚗🦾

Dự án này triển khai hệ thống điều khiển cho xe robot sử dụng 4 bánh **mecanum**, tích hợp **ROS 2**, **ESP32 (micro-ROS)**, giao thức **Modbus TCP**, và khả năng mở rộng điều hướng thông minh (SLAM, giao diện điều khiển, AI perception...).

## 🎯 Mục tiêu

- Điều khiển từng bánh của xe mecanum thông qua PWM (ESP32).
- Truyền nhận dữ liệu điều khiển qua **micro-ROS** (UART).
- Gửi lệnh tốc độ, hướng di chuyển từ giao diện web hoặc node ROS.
- Hỗ trợ feedback tốc độ, xung encoder, góc quay (yaw), dữ liệu IMU.
- Hướng đến tích hợp bản đồ, tìm đường và điều hướng tự động.

---

## 🛠️ Thành phần chính

### 1. Phần cứng
- **ESP32 Dev Module x2**: điều khiển motor và thu thập sensor.
- **Driver 2HSS57 + Motor 57J1880EC-1000**: động cơ có encoder 5000 pulse/vòng.
- **4 bánh Mecanum 100mm**: hỗ trợ di chuyển đa hướng.
- **Cảm biến GY-85 (IMU 9 trục)**: đo góc nghiêng và gia tốc.
- **RS485 / Bluetooth / Webserver / UART**: các giao thức kết nối.
- **Nguồn DC 24V**: cấp cho động cơ.

### 2. Phần mềm
- **ROS 2 Foxy / Humble**: hệ điều hành robot.
- **micro-ROS (PlatformIO)**: firmware điều khiển motor từ ESP32.
- **Python ROS2 Node**: gửi lệnh `freq_cmd`, nhận `output_log`.
- **Modbus TCP Server**: đọc các giá trị vận tốc, xung, IMU.
- **Web Interface**: nhập lệnh vị trí (X, Y), hướng (Yaw), tốc độ.
- **SLAM Toolbox**: để mở rộng mapping và localization.

---

