# KẾ HOẠCH THỰC HIỆN DỰ ÁN (3 TUẦN)

- **Đề tài:** Xây dựng hệ thống hỗ trợ quản lý và điều phối hoạt động thiện nguyện nội bộ cho công ty Unikom.
- **Công cụ:** Apache NetBeans, SQL Server, Java (JSP/Servlet), Tomcat.

---

## 1. Phân bổ vai trò (AI & Human)

| Giai đoạn | Nội dung | Vai trò chính |
| :--- | :--- | :--- |
| **Tuần 1** | Khảo sát, Thiết kế DB & UI | **AI:** Gợi ý cấu trúc bảng SQL, tạo Layout Bootstrap. **Người:** Cài đặt NetBeans, cấu hình Tomcat, tạo Database. |
| **Tuần 2** | Lập trình chức năng (Coding) | **AI:** Viết các hàm DAO (CRUD), Servlet mẫu. **Người:** Lập trình chức năng trên NetBeans, kết nối DB. |
| **Tuần 3** | Kiểm thử & Release | **AI:** Kiểm tra lỗi logic, gợi ý tối ưu code. **Người:** Test luồng dữ liệu, Clean & Build dự án. |

---

## 2. Lịch trình chi tiết

### Tuần 1: Thiết kế & Khởi tạo (Tập trung Database + UI)
- **Công việc:**
    - Phân tích yêu cầu: Admin tạo chiến dịch, User đăng ký đóng góp.
    - Thiết kế SQL Server: Tạo 3 bảng chính `Users`, `Campaigns`, `Donations`.
    - Khởi tạo Web Project trên **NetBeans** (Maven).
    - Tạo giao diện JSP: Dùng Bootstrap thiết kế trang chủ, trang Admin và trang Đóng góp.
- **AI làm chính:** Gợi ý SQL Script và mẫu giao diện Bootstrap.
- **Output:** Database hoàn thiện và bộ khung giao diện (Frontend).

### Tuần 2: Lập trình chức năng cốt lõi (Core Logic)
- **Công việc:**
    - Viết Class `DBContext` để kết nối SQL Server trong NetBeans.
    - Chức năng Admin: Thêm/Sửa/Xóa chiến dịch thiện nguyện (CRUD).
    - Chức năng User: Lưu thông tin đóng góp vào SQL Server qua JDBC.
- **AI hỗ trợ:** Viết nhanh các hàm xử lý SQL (DAO) và sửa lỗi Runtime.
- **Output:** Web chạy được các tính năng cơ bản, dữ liệu lưu được vào SQL Server.

### Tuần 3: Hoàn thiện & Đóng gói (Testing & Release)
- **Công việc:**
    - Kiểm thử (Test): Đảm bảo không lỗi khi nhập liệu và xử lý Servlet.
    - Chỉnh sửa giao diện lần cuối cho chuyên nghiệp.
    - Xuất file SQL và dùng tính năng **Clean & Build** của NetBeans để đóng gói dự án.
- **AI hỗ trợ:** Viết tài liệu hướng dẫn và tóm tắt tính năng.
- **Output:** Dự án hoàn thiện, sẵn sàng nộp bài báo cáo.










