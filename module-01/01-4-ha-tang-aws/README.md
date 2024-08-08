#### Một số khái niệm cần làm rõ

### 1. Availability zone
- Một `Availability zone (AZ)` bao gồm một hoặc nhiều trung tâm dữ liệu, các AZ được thiết kế để không xảy ra xự cố ảnh hưởng đồng thời 2 AZ cùng lúc (`fault isolation`).
- Giữa 2 AZ là đường kết nối riêng tốc độ cao
- AWS khuyến nghị nên triền khai ứng dụng tối thiểu trên 2 AZ.

### 2. Region
- Một số AWS Region bao gồm tối thiểu 3 Availability zone. Hiện tại có hơn 25 region trên toàn cầu.
- Các region được kết nối với nhau bởi mạng của backbone của aws
- Mặc định dữ liệu và dịch vụ của region đôc lập với nhau. (Trừ 1 số dịch vụ quy mô ở mức global)
- Lựa chọn region gần với người dùng nhất.
- Lưu ý khi chọn region dựa trên tri phí, quy mô càng lớn, càng nhiều người dùng thì càng rẻ.

### 3. Edge Locations
- Là mạng lưới trung tâm dữ liệu AWS được thiết kế để cung cấp dịch vụ với độ trễ thấp nhất có thể.
- Các loại dịch vụ AWS hoạt động tại Edge Locations (POP) bao gồm:
  - CloudFont (CDN)
  - Web Application Firewall (WAF)
  - Route 53 (DNS Service)