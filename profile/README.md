# 🚀 DỰ ÁN ROS2-DIFF-DRIVE-CONTROLLER CHO ROBOT MECANUM 4 BÁNH

## 🔍 TỔNG QUAN

Dự án xây dựng hệ thống điều khiển cho robot sử dụng 4 bánh **mecanum**, cho phép di chuyển linh hoạt đa hướng. Hệ thống ứng dụng **ROS 2**, **micro-ROS**, và các nền tảng phần cứng hiện đại như **ESP32**, **camera Intel RealSense D435i**, **cánh tay robot xArm Lite 6**, kết hợp với các kỹ thuật điều hướng thông minh (SLAM, base_link, odom…).

> Mục tiêu cuối cùng là tạo ra một robot có khả năng tự hành, định vị, điều khiển cơ cấu tay máy chính xác, và có khả năng giao tiếp mạnh mẽ qua các tầng ROS2 – vi điều khiển – mạng.

---

## 👥 THÀNH VIÊN THỰC HIỆN

| Họ và tên             | Vai trò |
|-----------------------|---------|
| Nguyễn Thanh Nhân (Leader)     |  Lập trình ROS2, micro-ROS, giao tiếp và điều khiển |
| Nguyễn Vũ Huy Khôi    | Lập trình Camera và huấn luyện mô hình YOLO |
| Hồ Đức An             | Điều phối phần cứng, thiết kế khung robot|
| **GVHD:** TS. Phạm Quốc Thiện | Hướng dẫn chuyên môn và kiểm tra tiến độ |

---

## 📆 TIẾN ĐỘ HOÀN THÀNH

| Công việc                                                                 | Trạng thái       |
|---------------------------------------------------------------------------|------------------|
| ✔️ Chuẩn bị phần cứng                                                     | Hoàn thành       |
| ✔️ Xây dựng khung phần cứng ban đầu                                       | Hoàn thành       |
| ✔️ Nâng cấp phần cứng lần 2                                               | Hoàn thành       |
| ✔️ Nâng cấp khung phần cứng lần 3                                         | Hoàn thành       |
| ✔️ Giao tiếp độc lập các module (Intel D435i, xArm Lite 6, ROS2, micro-ROS) | Hoàn thành       |
| ✔️ Xây dựng thành công Drive Controller cho robot                         | Hoàn thành       |
| ✔️ Nâng cấp phần cứng lần 3                                           | Hoàn thành   |
| - **Viết node xử lý dữ liệu IMU (BMX160)**                                | Đang tiến hành  |
| ❌ **Xây dựng hệ trục tọa độ `base_link → odom → map`**                  | Chưa hoàn thành  |
| ❌ **Triển khai SLAM (gmapping/slam_toolbox)**                            | Chưa hoàn thành  |
| ❌ **Xây dựng giao diện kiểm soát từ xa và bản đồ thời gian thực**       | Chưa hoàn thành  |

---

## ⏳ THỜI GIAN CÒN LẠI

> Tính từ **hôm nay (16/07/2025)** đến các deadline:

- 🟠 **DEADLINE 1: Tháng 9 năm 2025** → Còn **46 ngày**  
- 🔴 **DEADLINE 2: Tháng 9 năm 2026** → Còn **411 ngày**

> ⚠️ Cần ưu tiên hoàn thiện các module quan trọng trước mốc Deadline 1:
- Giao tiếp IMU
- Hệ quy chiếu base_link → odom → map
- Chạy thử SLAM và định vị cơ bản

---

## 📁 DỰ KIẾN MỞ RỘNG

- Điều khiển cơ cấu gắp dựa trên hình ảnh từ RealSense
- Tự động định hướng gắp vật với AI hỗ trợ
- Nhận diện bản đồ khu vực làm việc và tìm đường đi ngắn nhất
- Đồng bộ hóa hệ thống điều khiển với phần giám sát trung tâm (dashboard)

---

## 📜 GIẤY PHÉP SỬ DỤNG

Dự án này thuộc quyền sở hữu nhóm sinh viên và giáo viên hướng dẫn, sử dụng cho mục đích học thuật và nghiên cứu tại trường.

---


<script>(function(d, s, id) { var js, pjs = d.getElementsByTagName(s)[0]; if (d.getElementById(id)) return; js = d.createElement(s); js.id = id; js.src = "//www.tickcounter.com/static/js/loader.js"; pjs.parentNode.insertBefore(js, pjs); }(document, "script", "tickcounter-sdk"));</script><a data-type="countdown" data-id="7690151" class="tickcounter" style="display:block; left:0; width:100%; height:0; position:relative; padding-bottom:25%; margin:0 auto;" title="Đồ án tốt nghiệp" href="//www.tickcounter.com/">Đồ án tốt nghiệp</a>
