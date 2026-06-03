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

<img width="1056" height="679" alt="image" src="https://github.com/user-attachments/assets/8e836cc5-1e6b-47d3-bc3a-e53a54505262" />

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

**Biểu đồ tuần tự: quy trình "Đóng góp chiến dịch"**

<img width="1350" height="881" alt="image" src="https://github.com/user-attachments/assets/97ad0f74-b2a3-4235-aa3b-14ccb96463db" />

**Biểu đồ tuần tự: quy trình "Thêm mới chiến dịch"**

<img width="1250" height="915" alt="image" src="https://github.com/user-attachments/assets/6ae4d102-1967-46b0-afb4-07e95fccbe0e" />

**Biểu đồ tuần tự: quy trình "Chỉnh sửa/cập nhật chiến dịch"**

<img width="1282" height="898" alt="image" src="https://github.com/user-attachments/assets/37943548-a8f9-457c-9e1f-b7feeb112b26" />

## 7. Biểu đồ Class Diagram

<img width="817" height="716" alt="image" src="https://github.com/user-attachments/assets/520ad9c4-6b4c-4b3c-9edd-55d6ecb095f1" />

**A. Lớp User (Người dùng)**
Đóng vai trò quản lý thông tin tài khoản của toàn bộ các tác nhân truy cập vào hệ thống.

**Các thuộc tính:**

id: Mã định danh duy nhất của mỗi tài khoản (Khóa chính - Primary Key).

username, password: Tài khoản và mật khẩu mã hóa dùng để đăng nhập hệ thống.

fullName: Tên hiển thị đầy đủ của người dùng (Admin hoặc Nhà hảo tâm).

role: Phân quyền người dùng (Nhận giá trị "Admin" để vào trang quản trị hoặc "Donor" để thực hiện quyên góp).

**Các phương thức:**

login(): Xử lý nghiệp vụ kiểm tra tài khoản khi người dùng đăng nhập.

register(): Xử lý tạo tài khoản mới cho nhà hảo tâm.

**B. Lớp Campaign (Chiến dịch thiện nguyện)**
Đại diện cho các chương trình kêu gọi quyên góp do Admin khởi tạo và quản lý.

**Các thuộc tính:**

id: Mã định danh duy nhất của chiến dịch.

title: Tên của chiến dịch kêu gọi (Ví dụ: "Tết hồng cho em", "Mùa hè rực rỡ").

description: Bài viết mô tả chi tiết, mục đích của chiến dịch.

thumbnail: Đường dẫn lưu tên file ảnh minh họa của chiến dịch trên server.

targetAmount: Số tiền mục tiêu cần kêu gọi (VNĐ).

startDate, endDate: Ngày bắt đầu và ngày kết thúc chiến dịch nhằm phục vụ logic tự động tính toán trạng thái.

status: Trạng thái hiển thị (Đang diễn ra, Sắp diễn ra, Đã kết thúc).

**Các phương thức:**

createCampaign(), updateCampaign(), deleteCampaign(): Các hàm CRUD phục vụ quyền quản trị của Admin ngoài bộ điều khiển.

getCurrentTotalAmount(): Hàm tính toán, chạy câu lệnh cộng dồn (SUM) tổng số tiền thực tế đã nhận được từ các nhà hảo tâm để hiển thị thanh tiến độ.

**C. Lớp Donation (Lượt đóng góp/Quyên góp)**
Lớp trung gian lưu vết toàn bộ lịch sử các giao dịch đóng góp dòng tiền hoặc nhu yếu phẩm trong hệ thống.

**Các thuộc tính:**

id: Mã giao dịch quyên góp.

userId: ID của người thực hiện đóng góp (Khóa ngoại liên kết tới lớp User).

campaignId: ID của chiến dịch nhận tiền (Khóa ngoại liên kết tới lớp Campaign).

donationType: Hình thức ủng hộ ("Tiền mặt" hoặc "Hiện vật").

amount: Số tiền cụ thể đóng góp (bằng 0 nếu là hiện vật).

message: Lời chúc, tâm tình của nhà hảo tâm gửi tới chiến dịch.

donationDate: Thời gian hệ thống ghi nhận giao dịch thành công.

**Các phương thức:**

insertDonation(): Thực thi lệnh chèn một bản ghi giao dịch mới vào cơ sở dữ liệu khi bấm xác nhận.

getDonationsByUserId(), getDonationsByCampaignId(): Truy vấn danh sách giao dịch theo bộ lọc người dùng (để xem lịch sử cá nhân) hoặc theo chiến dịch (để Admin quản lý dòng tiền).
## 8. Thiết kế cơ sở dữ liệu
## 8.1 Bảng Users (Người dùng)

* **Ý nghĩa:** Lưu trữ thông tin tài khoản của toàn bộ thành viên truy cập hệ thống (bao gồm Quản trị viên và Nhà hảo tâm/Nhân viên).

| Tên trường | Kiểu dữ liệu | Ràng buộc | Mô tả |
| :--- | :--- | :--- | :--- |
| `user_id` | `INT` | `IDENTITY(1,1)`, `PRIMARY KEY` | Mã định danh duy nhất của người dùng (Tự động tăng). |
| `username` | `VARCHAR(50)` | `UNIQUE`, `NOT NULL` | Tên đăng nhập vào hệ thống (Không được trùng lặp). |
| `password` | `VARCHAR(50)` | `NOT NULL` | Mật khẩu đăng nhập. |
| `fullname` | `NVARCHAR(100)` | `NOT NULL` | Họ và tên đầy đủ của người dùng (Hỗ trợ tiếng Việt). |
| `email` | `VARCHAR(100)` | `NULL` | Địa chỉ thư điện tử của người dùng. |
| `role` | `VARCHAR(20)` | `DEFAULT 'USER'` | Phân quyền tài khoản trong hệ thống (`'ADMIN'` hoặc `'USER'`). |

---

## 8.2 Bảng `Campaigns` (Chiến dịch thiện nguyện)

* **Ý nghĩa:** Lưu trữ thông tin chi tiết về các chương trình, chiến dịch phát động kêu gọi quyên góp thiện nguyện.

| Tên trường | Kiểu dữ liệu | Ràng buộc | Mô tả |
| :--- | :--- | :--- | :--- |
| `campaign_id` | `INT` | `IDENTITY(1,1)`, `PRIMARY KEY` | Mã định danh duy nhất của chiến dịch (Tự động tăng). |
| `title` | `NVARCHAR(200)` | `NOT NULL` | Tên hoặc tiêu đề của chiến dịch thiện nguyện. |
| `description` | `NVARCHAR(MAX)` | `NULL` | Bài viết mô tả chi tiết nội dung, mục đích của chiến dịch. |
| `image_url` | `VARCHAR(250)` | `NULL` | Đường dẫn/tên file ảnh minh họa lưu trên server để hiển thị ngoài giao diện. |
| `start_date` | `DATE` | `NULL` | Ngày bắt đầu triển khai chiến dịch kêu gọi. |
| `end_date` | `DATE` | `NULL` | Ngày kết thúc chiến dịch nhận đóng góp. |
| `target_amount` | `DECIMAL(18,2)` | `DEFAULT 0` | Số tiền mục tiêu cần kêu gọi (Đơn vị: VNĐ). |
| `status` | `NVARCHAR(50)` | `DEFAULT N'Đang diễn ra'` | Trạng thái chiến dịch (`Đang diễn ra`, `Đã kết thúc`, `Sắp diễn ra`). |

---

## 8.3 Bảng `Donations` (Lịch sử đóng góp)

* **Ý nghĩa:** Lưu trữ chi tiết tất cả các lượt tham gia quyên góp của người dùng vào từng chiến dịch, hỗ trợ cả hình thức đóng góp bằng tiền mặt và hiện vật.

| Tên trường | Kiểu dữ liệu | Ràng buộc | Mô tả |
| :--- | :--- | :--- | :--- |
| `donation_id` | `INT` | `IDENTITY(1,1)`, `PRIMARY KEY` | Mã định danh duy nhất của lượt đóng góp (Tự động tăng). |
| `user_id` | `INT` | `FOREIGN KEY REFERENCES Users(user_id)` | Mã người đóng góp (Khóa ngoại liên kết tới bảng `Users`). |
| `campaign_id` | `INT` | `FOREIGN KEY REFERENCES Campaigns(campaign_id)` | Mã chiến dịch nhận đóng góp (Khóa ngoại liên kết tới bảng `Campaigns`). |
| `amount` | `DECIMAL(18,2)` | `NOT NULL` | Số tiền đóng góp (Bằng `0` nếu người dùng chỉ đóng góp hiện vật). |
| `donation_date` | `DATETIME` | `DEFAULT GETDATE()` | Ngày giờ hệ thống tự động ghi nhận giao dịch thành công. |
| `message` | `NVARCHAR(500)` | `NULL` | Lời nhắn, lời chúc của người đóng góp gửi tới chiến dịch. |
| `donation_type` | `VARCHAR(20)` | `DEFAULT 'CASH'` | Hình thức quyên góp (`'CASH'` - Tiền mặt hoặc `'ITEMS'` - Hiện vật). |
| `item_details` | `NVARCHAR(500)` | `NULL` | Thông tin mô tả chi tiết nếu chọn đóng góp bằng hiện vật (Ví dụ: Mì tôm, quần áo...). |

---

## 10. Testcase

[📥 Bấm vào đây để tải file Excel TESTCASE](TESTCASEdonggop.xlsx)

## 11. Kết quả đạt được

Trải qua quá trình nghiên cứu, phân tích thiết kế hệ thống hướng đối tượng và triển khai thực nghiệm, dự án xây dựng hệ thống Quản lý Chiến dịch Thiện nguyện dựa trên nền tảng Java Servlet và SQL Server đã hoàn thành đầy đủ các mục tiêu cá nhân đề ra ban đầu, cụ thể bao gồm:

### Về mặt Phân tích & Thiết kế (Analysis & Design)
* **Xây dựng kiến trúc phân lớp chuẩn hóa:** Hoàn thiện sơ đồ thực thể liên kết dữ liệu (Class Diagram/ERD) gồm các bảng cốt lõi (`Users`, `Campaigns`, `Donations`) loại bỏ hoàn toàn hiện tượng dư thừa dữ liệu, đồng bộ hóa tốt cấu trúc cơ sở dữ liệu quan hệ với các lớp Java Bean (POJO) của mã nguồn.
* **Mô hình hóa luồng nghiệp vụ chặt chẽ:** Thiết kế thành công hệ thống các biểu đồ tuần tự (Sequence Diagram) theo kiến trúc BCE (Boundary - Control - Entity), bao phủ toàn diện từ luồng xác thực đăng nhập người dùng, quy trình đóng góp có chọn lọc chiến dịch ngoài trang chủ, cho đến tập hợp các thao tác quản trị CRUD dành riêng cho quyền quản trị viên (Admin).

### Về mặt Chức năng & Giao diện (System Functions)
* **Phân hệ dành cho Nhà hảo tâm (User Side):**
    * Hệ thống xác thực và khởi tạo Session làm việc an toàn, quản lý tốt trạng thái đăng nhập.
    * Giao diện hiển thị danh sách các chiến dịch thiện nguyện trực quan, hiển thị rõ ràng thông tin số tiền mục tiêu, mốc thời gian và trạng thái thời gian thực.
    * Form đăng ký đóng góp xử lý linh hoạt hai hình thức hỗ trợ: Tiền mặt (`CASH`) và Hiện vật (`ITEMS`), tích hợp cơ chế Validate dữ liệu đầu vào nghiêm ngặt (Số tiền đóng góp bắt buộc phải lớn hơn 0).
* **Phân hệ dành cho Quản trị viên (Admin Side):**
    * Xây dựng trang Dashboard quản trị tập trung, hỗ trợ trọn vẹn nghiệp vụ Thêm mới, Sửa đổi thông tin (bao gồm cơ chế xử lý file ảnh minh họa `image_url`) và Xóa bỏ các chiến dịch khi cần thiết.
    * Hệ thống bộ lọc nâng cao cho phép xuất dữ liệu lịch sử đóng góp (Kết hợp phép `JOIN` dữ liệu đa bảng) hiển thị tường minh danh tính nhà hảo tâm, loại hình đóng góp và lời nhắn gửi đi kèm.

---

## 12. Định hướng phát triển

Dù hệ thống cơ bản đã vận hành ổn định và đáp ứng tốt các yêu cầu nghiệp vụ lõi, tác giả vẫn xác định được một số hạn chế nhất định và đề xuất các giải pháp nâng cấp, định hướng mở rộng mã nguồn trong tương lai như sau:

* **Tích hợp cổng thanh toán trực tuyến:** Thay vì ghi nhận giao dịch thủ công qua form điền số tiền, hệ thống định hướng tích hợp thêm các API cổng thanh toán phổ biến như VNPay, Momo hoặc ZaloPay để tự động hóa hoàn toàn quy trình chuyển tiền, tạo mã QR Code thanh toán động dựa trên `donation_id`.
* **Áp dụng Trí tuệ nhân tạo (AI):** Nghiên cứu tích hợp các mô hình Machine Learning cơ bản và công nghệ OCR (Nhận dạng ký tự quang học) nhằm hỗ trợ tự động quét/đọc minh chứng hóa đơn, biên lai chuyển khoản mà người dùng tải lên, giúp hệ thống tự động đối soát dòng tiền và nâng cao tính minh bạch tuyệt đối cho hoạt động giải ngân.
* **Tối ưu hóa kiến trúc và bảo mật:** Chuyển đổi mã nguồn từ kiến trúc Servlet/JSP truyền thống sang kiến trúc Single Page Application (SPA) sử dụng React hoặc VueJS cho Frontend, kết hợp Spring Boot làm RESTful API ở Backend. Đồng thời áp dụng mã hóa mật khẩu nâng cao (như BCrypt) thay vì lưu chuỗi text thô như hiện tại nhằm tối ưu tính an toàn thông tin người dùng.

---

## 13. kết luận

Dự án phát triển ứng dụng Quản lý Chiến dịch Thiện nguyện không chỉ giải quyết bài toán cấp thiết trong việc số hóa, minh bạch hóa các hoạt động quyên góp xã hội của tổ chức, mà còn là cơ hội thực tiễn quý báu giúp củng cố kiến thức toàn diện về quy trình phát triển phần mềm. 

Thông qua việc hiện thực hóa bài tập lớn từ các bước khảo sát yêu cầu, thiết kế biểu đồ ca sử dụng, vẽ biểu đồ lớp, biểu đồ tuần tự cho đến lập trình kết nối cơ sở dữ liệu, sinh viên đã nắm vững tư duy lập trình hướng đối tượng (OOP), làm chủ được cơ chế mô hình hóa hệ thống và cách thức quản lý mã nguồn độc lập trên môi trường GitHub. Những kết quả thực nghiệm đạt được chính là nền tảng vững chắc để tác giả tiếp tục phát triển thêm nhiều ứng dụng công nghệ thông tin có tính thực tiễn cao hơn nữa trong tương lai.


