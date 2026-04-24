<div align="center">
  <h1>Welcome to EraEstate</h1>
  <p><strong>The Next-Generation Real Estate Platform Ecosystem</strong></p>
</div>

EraEstate là một nền tảng PropTech (Property Technology) toàn diện, định nghĩa lại cách người dùng, đại lý (Agent) và các doanh nghiệp (Agency) tương tác trên thị trường bất động sản. Bằng cách kết hợp kiến trúc Microservices hiện đại, sức mạnh phân tích của Trí Tuệ Nhân Tạo (AI) và tính minh bạch tuyệt đối của công nghệ Web3, EraEstate mang đến một hệ sinh thái an toàn, thông minh và siêu tốc.

---

## <img src="./assets/rocket.svg" width="24" height="24" align="top" /> Tầm Nhìn & Sứ Mệnh

Thị trường bất động sản truyền thống thường gặp khó khăn về tính minh bạch, tốc độ giao dịch và thiếu các công cụ phân tích chuyên sâu. EraEstate ra đời để giải quyết triệt để những vấn đề này:
- **Minh bạch hóa giao dịch**: Ứng dụng Smart Contract và Web3 Escrow để loại bỏ rủi ro tài chính.
- **Tối ưu hóa trải nghiệm**: Mang lại các công cụ AI và bản đồ thông minh giúp khách hàng tìm kiếm chính xác nhu cầu.
- **Chuyên nghiệp hóa quản lý**: Cung cấp bộ công cụ CRM thu nhỏ cho các nhà môi giới và công ty bất động sản để quản lý tệp khách hàng và tin đăng.

---

## <img src="./assets/building.svg" width="24" height="24" align="top" /> Kiến Trúc Hệ Thống (System Architecture)

Hệ thống EraEstate được thiết kế dựa trên tiêu chuẩn Enterprise, đảm bảo tính mở rộng (Scalability) và độ khả dụng cao (High Availability):

### <img src="./assets/frontend.svg" width="18" height="18" align="top" /> 1. Lớp Trình Diễn (Frontend Layer)
- **Công nghệ cốt lõi**: React 18, TypeScript, Vite.
- **Giao diện & Trải nghiệm**: Sử dụng Tailwind CSS kết hợp với hệ thống Design Token riêng biệt, mang lại giao diện Dark/Light mode hiện đại.
- **Tương tác thời gian thực**: Cập nhật trạng thái thông báo và tin nhắn tức thời qua WebSockets.
- **Bản đồ không gian**: Tích hợp Leaflet cho phép tìm kiếm bất động sản theo đa giác (Polygon Search) và hiển thị các điểm tiện ích (POI).

### <img src="./assets/backend.svg" width="18" height="18" align="top" /> 2. Lớp Dịch Vụ Cốt Lõi (Core Backend Layer)
- **Công nghệ cốt lõi**: Java 21, Spring Boot 3.5.6, Spring Data JPA, Hibernate.
- **Quản trị cơ sở dữ liệu**: MariaDB cho dữ liệu quan hệ đồng thời tối ưu hóa các câu lệnh truy vấn phức tạp (JPQL).
- **Caching & Rate Limiting**: Triển khai Redis để lưu trữ Cache và giới hạn số lượng request API với thuật toán Token Bucket (thông qua Bucket4j), giúp ngăn chặn các cuộc tấn công DDoS và Brute-force.
- **Kiến trúc đồng bộ**: Xử lý logic nghiệp vụ chặt chẽ, từ quy trình duyệt tin, đánh giá, đến phân quyền đa cấp.

### <img src="./assets/blockchain.svg" width="18" height="18" align="top" /> 3. Lớp Giao Dịch & Bảo Mật Web3 (Web3 Security Layer)
- **Smart Contracts**: Viết bằng Solidity trên nền tảng Hardhat.
- **Web3 Escrow**: Cơ chế ký quỹ tự động. Tiền của người thuê/người mua được đóng băng trong Smart Contract và chỉ được giải ngân khi các điều khoản hợp đồng được đáp ứng, loại bỏ hoàn toàn lừa đảo.

---

## <img src="./assets/chart.svg" width="24" height="24" align="top" /> Tính Năng Cốt Lõi (Core Modules)

### <img src="./assets/ai.svg" width="18" height="18" align="top" /> Phân Tích & Định Giá (AI & Analytics)
- **Automated Valuation Models (AVM)**: Hệ thống tự động định giá bất động sản dựa trên lịch sử giao dịch và dữ liệu khu vực xung quanh.
- **Radar Charts & Heatmaps**: Trực quan hóa mức độ hấp dẫn của bất động sản thông qua biểu đồ Radar (so sánh tiện ích, giá, diện tích) và Bản đồ nhiệt (Heatmap) thể hiện khu vực đang sốt giá.

### <img src="./assets/map.svg" width="18" height="18" align="top" /> Tìm Kiếm Không Gian (Spatial Search)
- **Interactive POI Maps**: Hiển thị các tiện ích xung quanh (Trường học, Bệnh viện, Siêu thị) với khoảng cách thực tế.
- **Polygon Search**: Người dùng có thể dùng chuột khoanh vùng khu vực mong muốn trực tiếp trên bản đồ để lọc ra các bất động sản nằm chính xác trong vùng đó.

### <img src="./assets/subscription.svg" width="18" height="18" align="top" /> Quản Lý Gói Dịch Vụ (Subscription Lifecycle)
- **Quota Management**: Quản lý tự động giới hạn số lượng tin đăng, đẩy tin theo từng gói (Basic, Pro, Premium).
- **Automated Scheduler**: Hệ thống Cron-job liên tục quét và tự động khóa/hạ cấp các gói dịch vụ hết hạn, đồng thời gửi thông báo qua Email và hệ thống.

### <img src="./assets/chat.svg" width="18" height="18" align="top" /> Tương Tác Xã Hội (Social Platform)
- **Mạng xã hội thu nhỏ**: Cho phép người dùng theo dõi các Agent uy tín.
- **Messenger Module**: Tính năng chat Real-time với hỗ trợ gửi file, tìm kiếm tin nhắn, ghim tin nhắn, và sử dụng hệ thống icon reaction thuần SVG (không phụ thuộc font hệ thống).

### <img src="./assets/payment.svg" width="18" height="18" align="top" /> Thanh Toán Đa Dạng (Payment Gateway)
- Hỗ trợ thanh toán truyền thống qua cổng **VNPay**.
- Hỗ trợ thanh toán phi tập trung qua **Ví Crypto** cho các giao dịch quốc tế hoặc yêu cầu bảo mật cao.

---

## <img src="./assets/shield.svg" width="24" height="24" align="top" /> Tiêu Chuẩn Bảo Mật (Security Standards)

Bảo mật là ưu tiên hàng đầu tại EraEstate, đạt tiêu chuẩn cấp Enterprise:
- **Authentication**: JWT-based Dual Token System (Access Token & Refresh Token ngắn/dài hạn).
- **Authorization**: Role-Based Access Control (RBAC) với phân quyền chi tiết (Method-level security).
- **Protection**: Tích hợp phòng chống CSRF, XSS, và SQL Injection. Redis-based Rate Limiting để giới hạn Request ở cả cấp độ API công khai và API quản trị.
- **Data Privacy**: Mã hóa mật khẩu chuẩn BCrypt, quản lý các phiên làm việc (Session tracking) và tự động thu hồi token khi phát hiện hoạt động bất thường.

---

## <img src="./assets/globe.svg" width="24" height="24" align="top" /> Toàn Cầu Hóa (Internationalization)

Nền tảng hỗ trợ **19 ngôn ngữ** khác nhau thông qua thư viện `i18next`, tự động nhận diện khu vực và cho phép chuyển đổi ngôn ngữ mượt mà không cần tải lại trang. Các dữ liệu định dạng tiền tệ (Currency) và ngày tháng (Date/Time) cũng được tự động locale theo ngôn ngữ đã chọn.

---

### <img src="./assets/backend.svg" width="24" height="24" align="top" /> Tech Stack Summary

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-B73BFE?style=for-the-badge&logo=vite&logoColor=FFD62E)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-F2F4F9?style=for-the-badge&logo=spring-boot)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Web3](https://img.shields.io/badge/Web3-F16822?style=for-the-badge&logo=web3.js&logoColor=white)
![Solidity](https://img.shields.io/badge/Solidity-363636?style=for-the-badge&logo=solidity&logoColor=white)

---
*EraEstate - Kiến tạo niềm tin, nâng tầm giá trị bất động sản.*
