# KẾ HOẠCH THỰC HIỆN DỰ ÁN (3 TUẦN)
- **Đề tài:** Xây dựng hệ thống hỗ trợ quản lý và điều phối hoạt động thiện nguyện nội bộ cho công ty Unikom.
- **Công cụ:** VS Code, SQL Server, Java (JSP/Servlet)

## 1. Phân bổ vai trò (AI & Human)

| Giai đoạn | Nội dung | Vai trò chính |
| :--- | :--- | :--- |
| **Tuần 1** | Khảo sát, Thiết kế DB & UI | **AI:** Gợi ý cấu trúc bảng SQL, tạo Layout Bootstrap. **Người:** Cài đặt môi trường VS Code, tạo Database. |
| **Tuần 2** | Lập trình chức năng (Coding) | **AI:** Viết các hàm DAO (CRUD), Servlet mẫu. **Người:** Lắp ghép code, kết nối DB, fix lỗi logic. |
| **Tuần 3** | Kiểm thử & Release | **AI:** Viết tài liệu README, kiểm tra lỗi bảo mật. **Người:** Test luồng dữ liệu, nộp bài. |

## 2. Lịch trình chi tiết

### Tuần 1: Thiết kế & Khởi tạo (Tập trung Database + UI)
- **Công việc:**
    - Phân tích yêu cầu: Admin tạo chiến dịch, User đăng ký đóng góp.
    - Thiết kế SQL Server: 3 bảng chính (`Users`, `Campaigns`, `Donations`).
    - Tạo giao diện JSP: Trang chủ (danh sách), Trang Admin (quản lý), Trang Đóng góp.
- **AI làm chính:** Gợi ý code SQL Script và mẫu giao diện Bootstrap.
- **Output:** Database hoàn thiện và bộ khung giao diện (Frontend).

### Tuần 2: Lập trình chức năng cốt lõi (Core Logic)
- **Công việc:**
    - Viết Class kết nối SQL Server trong VS Code.
    - Chức năng Admin: Thêm/Sửa/Xóa chiến dịch thiện nguyện.
    - Chức năng User: Lưu thông tin đóng góp (số tiền, hiện vật) vào DB.
- **AI hỗ trợ:** Hỗ trợ viết nhanh các hàm xử lý SQL (JDBC) và sửa lỗi (Debug).
- **Output:** Web chạy được các tính năng cơ bản, dữ liệu lưu được vào SQL Server.

### Tuần 3: Hoàn thiện & Đóng gói (Testing & Release)
- **Công việc:**
    - Kiểm thử (Test): Đảm bảo không lỗi khi nhập liệu.
    - Chỉnh sửa giao diện lần cuối cho chuyên nghiệp.
    - Xuất file SQL và chuẩn bị tài liệu báo cáo.
- **AI hỗ trợ:** Viết file hướng dẫn sử dụng (README.md) và tóm tắt các tính năng chính.
- **Output:** Dự án hoàn thiện trên GitHub, sẵn sàng bàn giao/báo cáo.



  *Ghi chú: Kế hoạch có thể thay đổi tùy theo tiến độ thực tế.*
