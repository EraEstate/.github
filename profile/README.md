<div align="center">
  <h1>Welcome to EraEstate</h1>
  <p><strong>The Next-Generation Real Estate Platform Ecosystem</strong></p>
  <p>
    <img src="https://img.shields.io/badge/Status-Active-success.svg?style=for-the-badge" />
    <img src="https://img.shields.io/badge/Architecture-Microservices-blue.svg?style=for-the-badge" />
    <img src="https://img.shields.io/badge/Version-1.0.0-orange.svg?style=for-the-badge" />
  </p>
</div>

EraEstate là một nền tảng PropTech (Property Technology) toàn diện, định nghĩa lại cách người dùng, đại lý (Agent) và các doanh nghiệp (Agency) tương tác trên thị trường bất động sản. Bằng cách kết hợp kiến trúc Microservices hiện đại, sức mạnh phân tích của Trí Tuệ Nhân Tạo (AI) và tính minh bạch tuyệt đối của công nghệ Web3, EraEstate mang đến một hệ sinh thái an toàn, thông minh và siêu tốc.

---

## <img src="./assets/rocket.svg" width="24" height="24" align="top" /> Tầm Nhìn & Sứ Mệnh (Vision & Mission)

Thị trường bất động sản truyền thống thường gặp khó khăn về tính minh bạch, tốc độ giao dịch và thiếu các công cụ phân tích chuyên sâu. EraEstate ra đời để giải quyết triệt để những vấn đề này:

- **Minh bạch hóa giao dịch**: Ứng dụng Smart Contract và Web3 Escrow để loại bỏ rủi ro tài chính, bảo vệ cả người mua và người bán.
- **Tối ưu hóa trải nghiệm**: Mang lại các công cụ AI và bản đồ thông minh giúp khách hàng tìm kiếm chính xác nhu cầu một cách trực quan.
- **Chuyên nghiệp hóa quản lý**: Cung cấp bộ công cụ CRM thu nhỏ cho các nhà môi giới và công ty bất động sản để quản lý tệp khách hàng, quản lý quota tin đăng hiệu quả.

---

## <img src="./assets/workflow.svg" width="24" height="24" align="top" /> Luồng Nghiệp Vụ (System Workflow)

EraEstate không chỉ là một ứng dụng tìm kiếm, mà là một chuỗi cung ứng kỹ thuật số hoàn chỉnh cho bất động sản:

1. **Khám Phá (Discovery)**: Người dùng tìm kiếm bất động sản thông qua bộ lọc thông minh đa chiều, kết hợp bản đồ vệ tinh và mô hình gợi ý tự động (Recommendation Engine).
2. **Tương Tác (Engagement)**: Giao tiếp trực tiếp với đại lý (Agent) thông qua hệ thống Chat Real-time tích hợp sẵn, chia sẻ các danh sách (Favorites) và đàm phán giá cả.
3. **Giao Dịch (Transaction)**: Khởi tạo các hợp đồng điện tử (E-contracts) và thực hiện thanh toán an toàn thông qua cổng thanh toán VNPay hoặc ký quỹ tiền mã hóa (Web3 Escrow).
4. **Hậu Mãi (After-sales)**: Quản lý đánh giá, hệ thống tích điểm và gửi phản hồi tự động.

---

## <img src="./assets/building.svg" width="24" height="24" align="top" /> Kiến Trúc Hệ Thống (Enterprise Architecture)

Hệ thống EraEstate được thiết kế dựa trên tiêu chuẩn Enterprise, đảm bảo tính mở rộng (Scalability) và độ khả dụng cao (High Availability):

### <img src="./assets/frontend.svg" width="18" height="18" align="top" /> 1. Lớp Trình Diễn (Frontend Interface Layer)
- **Công nghệ cốt lõi**: React 18, TypeScript, Vite.
- **Quản lý State & Data Fetching**: Tối ưu hóa render vòng đời component, sử dụng caching phía client để mang lại tốc độ phản hồi tính bằng mili-giây.
- **Giao diện & Trải nghiệm (UI/UX)**: Sử dụng Tailwind CSS kết hợp với hệ thống Design Token riêng biệt, mang lại giao diện Dark/Light mode hiện đại. Toàn bộ icon được sử dụng dưới định dạng SVG thuần giúp giảm thiểu tối đa dung lượng tải trang.
- **Bản đồ không gian**: Tích hợp Leaflet cho phép tìm kiếm bất động sản theo đa giác (Polygon Search) và hiển thị các điểm tiện ích (POI).

### <img src="./assets/backend.svg" width="18" height="18" align="top" /> 2. Lớp Dịch Vụ Cốt Lõi (Core Backend Services)
- **Công nghệ cốt lõi**: Java 21, Spring Boot 3.5.x, Spring Data JPA, Hibernate.
- **Quản trị cơ sở dữ liệu**: PostgreSQL cho dữ liệu quan hệ, được thiết kế chuẩn hóa (Normalization) đồng thời tối ưu hóa các câu lệnh truy vấn phức tạp (JPQL/Native Queries) thông qua Indexing.
- **Caching & Giảm Tải**: Triển khai Redis để lưu trữ in-memory cache cho các dữ liệu ít thay đổi (ví dụ: cấu hình hệ thống, danh sách tính năng).
- **Rate Limiting**: Giới hạn số lượng request API với thuật toán Token Bucket (thông qua Bucket4j), giúp ngăn chặn các cuộc tấn công DDoS và Brute-force.
- **Kiến trúc đồng bộ**: Xử lý logic nghiệp vụ chặt chẽ, từ quy trình duyệt tin, tự động hóa package expiration (SubscriptionScheduler), đến phân quyền đa cấp.

### <img src="./assets/blockchain.svg" width="18" height="18" align="top" /> 3. Lớp Giao Dịch & Bảo Mật Web3 (Web3 Security Layer)
- **Smart Contracts**: Viết bằng ngôn ngữ Solidity trên nền tảng framework Hardhat.
- **Web3 Escrow**: Cơ chế ký quỹ tự động hoàn toàn phi tập trung. Tiền của người thuê/người mua được đóng băng trong Smart Contract và chỉ được giải ngân khi các điều khoản hợp đồng được đáp ứng, loại bỏ hoàn toàn khả năng lừa đảo (Trustless).

---

## <img src="./assets/feature.svg" width="24" height="24" align="top" /> Tính Năng Đột Phá (Advanced Features)

### <img src="./assets/ai.svg" width="18" height="18" align="top" /> Trí Tuệ Nhân Tạo & Phân Tích Dữ lưu (AI & Analytics)
- **Automated Valuation Models (AVM)**: Hệ thống tự động định giá bất động sản dựa trên lịch sử giao dịch và dữ liệu khu vực xung quanh.
- **Radar Charts & Heatmaps**: Trực quan hóa mức độ hấp dẫn của bất động sản thông qua biểu đồ Radar (so sánh tiện ích, giá, diện tích) và Bản đồ nhiệt (Heatmap) thể hiện khu vực đang sốt giá.

### <img src="./assets/map.svg" width="18" height="18" align="top" /> Hệ Thống Bản Đồ Không Gian (Spatial Search System)
- **Interactive POI Maps**: Hiển thị các tiện ích xung quanh (Trường học, Bệnh viện, Siêu thị) với khoảng cách thực tế.
- **Polygon Search**: Tính năng cao cấp cho phép người dùng dùng chuột khoanh vùng khu vực mong muốn trực tiếp trên bản đồ để lọc ra các bất động sản nằm chính xác trong vùng đó.

### <img src="./assets/subscription.svg" width="18" height="18" align="top" /> Quản Lý Doanh Nghiệp & Đại Lý (Subscription & Quota Management)
- **Hệ thống phân cấp**: Cung cấp các gói dịch vụ (Basic, Pro, Premium) với quyền lợi khác nhau.
- **Quota Control**: Quản lý tự động giới hạn số lượng tin đăng, số lượng tin đẩy (Boost) theo từng gói. Tính năng tự động ẩn bài viết khi vượt quá quota hoặc gói hết hạn.
- **Automated Scheduler**: Hệ thống Cron-job liên tục quét để tự động khóa/hạ cấp các gói dịch vụ, đồng thời kích hoạt các Webhook thông báo.

### <img src="./assets/chat.svg" width="18" height="18" align="top" /> Mạng Xã Hội Giao Dịch (Transactional Social Platform)
- **Kết nối Agent - Client**: Cho phép người dùng theo dõi các Agent uy tín.
- **Messenger Module**: Tính năng chat Real-time mạnh mẽ với hỗ trợ gửi file, tìm kiếm nội dung tin nhắn, ghim tin nhắn quan trọng, và sử dụng hệ thống icon reaction thuần SVG.

### <img src="./assets/payment.svg" width="18" height="18" align="top" /> Thanh Toán Đa Kênh (Omnichannel Payment Gateway)
- Tích hợp cổng thanh toán nội địa **VNPay** hỗ trợ thẻ tín dụng, ATM.
- Hỗ trợ thanh toán phi tập trung qua **Ví Crypto** (Metamask, TrustWallet) cho các giao dịch xuyên biên giới.

---

## <img src="./assets/shield.svg" width="24" height="24" align="top" /> Tiêu Chuẩn Bảo Mật (Enterprise Security Standards)

Hệ thống tuân thủ các tiêu chuẩn bảo mật khắt khe nhất của một hệ thống tài chính:
- **Authentication Lifecycle**: JWT-based Dual Token System (Access Token & Refresh Token ngắn/dài hạn) với cơ chế Token Rotation.
- **Authorization**: Role-Based Access Control (RBAC) với phân quyền chi tiết tới từng API (Method-level security `@PreAuthorize`).
- **Data Protection**: Tích hợp phòng chống CSRF, XSS, và SQL Injection. Tất cả mật khẩu được mã hóa Salt & Hash bằng BCrypt.
- **Session Management**: Quản lý các phiên làm việc (Session tracking) chủ động, giới hạn thiết bị đăng nhập, tự động thu hồi token khi phát hiện hoạt động bất thường.

---

## <img src="./assets/globe.svg" width="24" height="24" align="top" /> Hỗ Trợ Đa Ngôn Ngữ (Global Internationalization)

Nhằm tiếp cận khách hàng quốc tế, nền tảng hỗ trợ tự động **19 ngôn ngữ** khác nhau thông qua thư viện `i18next`. Hệ thống tự động nhận diện khu vực và cho phép chuyển đổi ngôn ngữ mượt mà không tải lại trang. Các dữ liệu về tiền tệ (Currency formatter) và ngày tháng (Date/Time localization) được tự động điều chỉnh theo locale tương ứng.

---

### <img src="./assets/code.svg" width="24" height="24" align="top" /> Hệ Sinh Thái Công Nghệ (Technology Stack Summary)

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-B73BFE?style=for-the-badge&logo=vite&logoColor=FFD62E)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-F2F4F9?style=for-the-badge&logo=spring-boot)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)

![Web3](https://img.shields.io/badge/Web3-F16822?style=for-the-badge&logo=web3.js&logoColor=white)
![Solidity](https://img.shields.io/badge/Solidity-363636?style=for-the-badge&logo=solidity&logoColor=white)

---
*EraEstate - Kiến tạo niềm tin, nâng tầm giá trị bất động sản.*
