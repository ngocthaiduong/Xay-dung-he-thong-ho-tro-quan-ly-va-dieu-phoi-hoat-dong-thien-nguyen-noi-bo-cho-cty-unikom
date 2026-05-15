# PHÂN TÍCH CHI TIẾT HỆ THỐNG HỖ TRỢ QUẢN LÝ VÀ ĐIỀU PHỐI HOẠT ĐỘNG THIỆN NGUYỆN NỘI BỘ CHO CTY UNIKOM

## 1. Giới thiệu bài toán

**1.1. Bối cảnh và Thực trạng**
Hoạt động thiện nguyện là một phần quan trọng trong văn hóa doanh nghiệp tại Unikom, thể hiện trách nhiệm xã hội và tinh thần đoàn kết của tập thể nhân viên. Tuy nhiên, hiện nay việc tổ chức và điều phối các hoạt động này vẫn đang gặp phải một số hạn chế:

- Quy trình thủ công: Việc thông báo, đăng ký tham gia và đóng góp hiện vật/tài chính chủ yếu thực hiện qua các kênh rời rạc (email, chat, bảng tin), dẫn đến thất lạc thông tin hoặc chậm trễ trong cập nhật dữ liệu.

- Thiếu tính minh bạch: Nhân viên khó có thể theo dõi trực tiếp tiến độ quyên góp hoặc cách thức phân bổ nguồn lực trong thời gian thực.

- Khó khăn trong quản lý: Ban tổ chức mất nhiều thời gian để tổng hợp số liệu, lập báo cáo thống kê và lưu trữ lịch sử các chiến dịch đã thực hiện.

**1.2. Mục tiêu dự án**
Xuất phát từ thực trạng trên, dự án "Xây dựng hệ thống hỗ trợ quản lý và điều phối hoạt động thiện nguyện nội bộ cho công ty Unikom" được triển khai nhằm:

- Số hóa quy trình: Xây dựng một nền tảng tập trung để quản lý toàn bộ vòng đời của một chiến dịch thiện nguyện từ khâu khởi tạo đến khi kết thúc.

- Tối ưu hóa tương tác: Giúp nhân viên dễ dàng tiếp cận thông tin, đăng ký đóng góp và nhận thông báo chỉ với vài thao tác đơn giản trên giao diện web.

- Đảm bảo tính minh bạch: Tự động hóa việc cập nhật số liệu quyên góp, giúp mọi thành viên trong công ty đều có thể giám sát tiến độ và sự đóng góp của tập thể.

**1.3. Phạm vi và Giải pháp**
Trong khuôn khổ dự án (thực hiện trong 03 tuần), hệ thống sẽ tập trung vào các module cốt lõi:

- Quản lý Chiến dịch: Cho phép Admin tạo, chỉnh sửa và điều phối các đợt thiện nguyện.

- Cổng Đóng góp: Giao diện dành cho nhân viên thực hiện ủng hộ và theo dõi danh sách đóng góp.

- Báo cáo Tổng hợp: Hệ thống tự động thống kê nguồn lực thu được để phục vụ công tác minh bạch tài chính.

## 2. Phân tích đối tượng (Actors)
Hệ thống tập trung vào 02 đối tượng chính:
1. **Admin (Ban điều hành/HR):** Người tạo ra các chiến dịch, quản lý ngân sách và phê duyệt đóng góp.
2. **User (Nhân viên Unikom):** Người theo dõi thông tin, thực hiện đăng ký tham gia hoặc ủng hộ tài chính/hiện vật.

## 3. Danh sách các Use Case chính

| STT | Use Case | Người thực hiện | Mô tả tóm tắt |
| :--- | :--- | :--- | :--- |
| 1 | Quản lý chiến dịch | Admin | Tạo mới, sửa, xóa các đợt thiện nguyện (Tên, mục tiêu, thời hạn). |
| 2 | Đăng ký đóng góp | User | Nhập số tiền hoặc hiện vật muốn ủng hộ cho một chiến dịch cụ thể. |
| 3 | Theo dõi tiến độ | User/Admin | Xem biểu đồ hoặc số liệu phần trăm hoàn thành mục tiêu chiến dịch. |
| 4 | Thống kê báo cáo | Admin | Xuất danh sách nhân viên đã đóng góp để minh bạch tài chính. |

## 4. Biểu đồ Use Case 

<img width="829" height="609" alt="image" src="https://github.com/user-attachments/assets/3ead4cdf-4089-46b7-b573-f493ff1b9944" />

**Giải thích các thành phần trong sơ đồ:**

**Actors (Tác nhân):**

- Nhân viên Unikom: Là người dùng, mục tiêu chính là tiếp nhận thông tin và thực hiện ủng hộ.

- Quản trị viên: Thường là nhân sự hoặc Ban điều hành, có quyền vận hành hệ thống.

**Giải thích các Use Case quan trọng:**

- Quản lý chiến dịch: Đây là chức năng Admin dùng để Thêm, Sửa, Xóa các cuộc vận động thiện nguyện.

- Đăng ký đóng góp: Chức năng cốt lõi giúp hệ thống ghi nhận số tiền/hiện vật từ nhân viên vào SQL Server.

- Xác nhận đóng góp: Một bước quan trọng để đảm bảo tính minh bạch. Admin sẽ xác nhận khi thực tế đã nhận được nguồn lực.

- Thống kê & Xuất báo cáo: Tự động hóa việc tổng hợp dữ liệu, thay thế cho việc làm báo cáo thủ công.

**Quan hệ Include/Extend:**

- Include (Bao gồm): Để thực hiện đóng góp hay quản lý, người dùng bắt buộc phải qua bước Đăng nhập.

- Extend (Mở rộng): Việc xác nhận đóng góp chỉ xảy ra sau khi có dữ liệu đăng ký đóng góp từ nhân viên.

## 5. Biểu đồ Activity Diagram

**5.1 Biểu đồ Hoạt động: Quy trình Đăng ký Đóng góp (User)**

<img width="644" height="592" alt="image" src="https://github.com/user-attachments/assets/fae93ae8-56f4-4e5a-8e57-6cea6b70d51d" />

**5.2 Biểu đồ Hoạt động: Quản lý Chiến dịch (Admin)**

<img width="627" height="610" alt="image" src="https://github.com/user-attachments/assets/ff3b7b56-e5c8-4f70-9636-644a2c3adc73" />

## 6. Biểu đồ Sequence Diagram

**Biểu đồ tuần tự: quy trình "Đăng ký đóng góp"**

<img width="709" height="641" alt="image" src="https://github.com/user-attachments/assets/bb7a90e9-f987-490b-99f5-ac44499b3cd1" />

