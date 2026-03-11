# Hệ Thống Quản Lý Chung Cư (Apartment Management System)

Một hệ thống phần mềm toàn diện được xây dựng để giúp ban quản lý chung cư dễ dàng theo dõi, điều hành và quản lý các hoạt động hàng ngày như quản lý căn hộ, cư dân, các khoản thu phí, thông báo và báo cáo doanh thu.

---

## Tính năng chính

- **Quản lý Cư dân & Tài khoản:** Thêm, sửa, xóa thông tin cư dân và quản lý phân quyền tài khoản (Admin/Resident).
- **Quản lý Căn hộ:** Quản lý danh sách, trạng thái và chi tiết các căn hộ trong tòa nhà.
- **Quản lý Phí & Thanh toán:** Theo dõi các khoản phí (phí dịch vụ, điện, nước, đóng góp...), xuất hóa đơn và quản lý lịch sử thanh toán.
- **Tích hợp Thanh toán QR Code:** Hỗ trợ tạo mã QR để cư dân thanh toán nhanh chóng và tiện lợi.
- **Thông báo & Liên lạc:** Gửi thông báo đến cư dân trên hệ thống và tích hợp gửi Email tự động.
- **Bảng điều khiển (Dashboard):** Thống kê trực quan về doanh thu, tình trạng thanh toán và báo cáo tổng quan bằng biểu đồ.
- **Bảo mật:** Xác thực và phân quyền người dùng an toàn bằng JWT (JSON Web Token).

---

## Công nghệ sử dụng

### Trái tim của hệ thống (Backend)
- **Ngôn ngữ:** Java 17+
- **Framework:** Spring Boot, Spring Security
- **Bảo mật:** JWT (JSON Web Token)
- **Quản lý dependencies:** Maven
- **Cơ sở dữ liệu:** SQL (Sử dụng file `QLCC.sql` được đính kèm)

### Giao diện người dùng (Frontend)
- **Thư viện chính:** React.js
- **UI Framework:** Material Dashboard 2 React (Material UI)
- **Ngôn ngữ/Cú pháp:** JavaScript (ES6+), HTML5, CSS3

---

## Cấu trúc thư mục

```text
Apartment_Management/
├── backend/                  # Mã nguồn Backend (Spring Boot)
│   ├── src/main/java/...     # Chứa Controllers, Models, Repositories, Services, Security...
│   ├── src/main/resources/   # Chứa cấu hình ứng dụng (application.properties)
│   └── pom.xml               # Cấu hình Maven
├── frontend/                 # Mã nguồn Frontend (ReactJS)
│   ├── public/               # File public, index.html, assets
│   ├── src/                  # Chứa Components, Layouts, Assets, Routes, Context...
│   └── package.json          # Danh sách thư viện NPM
├── QLCC.sql                  # File script cơ sở dữ liệu
└── README.md                 # Tài liệu dự án
```

## Hướng dẫn cài đặt và khởi chạy
Để chạy dự án này trên máy tính của bạn, vui lòng làm theo các bước dưới đây:

### 1. Yêu cầu hệ thống (Prerequisites)
- Java JDK 17+
- Node.js & npm (Khuyến nghị bản LTS)
- Hệ quản trị CSDL (MySQL / SQL Server)

### 2. Thiết lập Cơ sở dữ liệu
- Mở hệ quản trị CSDL của bạn (Ví dụ: MySQL Workbench).
- Tạo một database mới (ví dụ: qlcc).
- Chạy file script QLCC.sql nằm ở thư mục gốc để khởi tạo các bảng và dữ liệu mẫu.

### 3. Khởi chạy Backend
- Di chuyển vào thư mục backend:
```Bash
cd backend
```
- Mở file backend/src/main/resources/application.properties và cập nhật thông tin kết nối Database của bạn (URL, Username, Password).
- Chạy ứng dụng Spring Boot:
```Bash
./mvnw spring-boot:run
```
Backend thường sẽ chạy trên cổng `http://localhost:8080`.

### 4. Khởi chạy Frontend
- Mở một terminal mới và di chuyển vào thư mục frontend:
```Bash
cd frontend
```
- Cài đặt các gói thư viện (dependencies):
```Bash
npm install
# hoặc: yarn install
```
- Khởi động ứng dụng React:
```Bash
npm start
# hoặc: yarn start
```
Frontend sẽ tự động mở trên trình duyệt tại `http://localhost:3000`
