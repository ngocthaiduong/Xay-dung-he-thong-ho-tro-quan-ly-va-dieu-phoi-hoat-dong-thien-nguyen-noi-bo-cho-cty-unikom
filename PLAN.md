# KẾ HOẠCH THỰC HIỆN DỰ ÁN (4 TUẦN)
**Đề tài:** Xây dựng hệ thống hỗ trợ quản lý và điều phối hoạt động thiện nguyện nội bộ cho cty unikom

## 1. Công nghệ sử dụng
- **IDE:** NetBeans (Java Web - JSP/Servlet).
- **Database:** Microsoft SQL Server.
- **Thư viện kết nối:** JDBC (sqljdbc4.jar hoặc mssql-jdbc).
- **Giao diện:** HTML, CSS, Bootstrap (nhúng trực tiếp vào JSP).

## 2. Lịch trình chi tiết

### Tuần 1: Thiết kế Cơ sở dữ liệu & Kết nối (Database Focus)
- [ ] Thiết kế các bảng trong SQL Server: `Users`, `Campaigns`, `Donations`.
- [ ] Tạo Database, thiết lập Primary Key, Foreign Key.
- [ ] Viết Class `DBContext.java` trong NetBeans để kết nối SQL Server.
- [ ] Tạo các Model (Java Class) tương ứng với các bảng trong DB.

### Tuần 2: Xây dựng chức năng Admin (Quản lý chiến dịch)
- [ ] Xây dựng trang `AdminDashboard.jsp` hiển thị danh sách chiến dịch.
- [ ] Chức năng **Thêm mới** chiến dịch (Insert vào SQL Server).
- [ ] Chức năng **Sửa/Xóa** chiến dịch (Update/Delete).
- [ ] Sử dụng DAO (Data Access Object) để xử lý các câu lệnh SQL.

### Tuần 3: Xây dựng chức năng User (Đóng góp)
- [ ] Xây dựng trang chủ `Home.jsp` để nhân viên xem danh sách các hoạt động thiện nguyện.
- [ ] Xây dựng trang `DonationForm.jsp`: Cho phép nhân viên nhập số tiền/hiện vật.
- [ ] Xử lý Servlet để lưu dữ liệu đóng góp vào bảng `Donations` trong SQL.
- [ ] Hiển thị danh sách những người đã đóng góp (để đảm bảo tính minh bạch).

### Tuần 4: Tổng kết & Hoàn thiện
- [ ] Kiểm tra tính toàn vẹn dữ liệu (ví dụ: không cho đóng góp số tiền âm).
- [ ] Trang trí lại giao diện bằng Bootstrap cho chuyên nghiệp.
- [ ] Viết tài liệu hướng dẫn (README) và chuẩn bị file SQL Script để thầy có thể chạy thử.
- [ ] Nộp bài.

## 3. Cấu trúc bảng SQL Server
- **Users**: `UserID`, `FullName`, `Role` (Admin/User).
- **Campaigns**: `CampaignID`, `Title`, `Description`, `TargetAmount`, `Status`.
- **Donations**: `DonationID`, `UserID`, `CampaignID`, `Amount`, `Date`.

  *Ghi chú: Kế hoạch có thể thay đổi tùy theo tiến độ thực tế.*
