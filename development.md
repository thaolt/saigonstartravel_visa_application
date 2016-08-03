# Thiết kế & Xây dựng website SaigonStar Travel

## Yêu cầu tổng quan {#overview}

Công ty SaigonStar Travel muốn có một giải pháp cho phép người sử dụng có thể gởi yêu cầu đăng ký Visa đến Việt Nam trực tuyến và nhận phản hồi qua email thông qua dịch vụ web của công ty. Khách hàng có thể thanh toán phí dịch vụ trực tiếp trên website của SaigonStar Travel.

### Mục tiêu

- Khách quan tâm có thể thăm trang web và xem danh sách các loại đơn xin Visa với các mục đích khác nhau như: du lịch, công tác, thăm thân, v.v..
- Khách hàng có thể gởi đơn yêu cầu xin Visa trực tiếp trên trang web.
- Cho phép thanh toán trực tuyến ( đối tượng khách hàng khách Châu Âu đang muốn đến Việt Nam ).
- Có kế hoạch marketing trực tuyến cho website giúp đến gần với đối tượng khách hàng tiềm năng hơn.
- Tích hợp sẵn 4 ngôn ngữ: Anh, Pháp, Đức, Tây Ban Nha ( cho phép quản trị tự thêm ngôn ngữ ).
- Trang web phải có bảo mật và độ an toàn dữ liệu cao.
- Có sử dụng công cụ theo dõi và báo cáo tình trạng khách viếng thăm website.

### Thiết kế

- Có giao diện được thiết kế sáng sủa đơn giản dễ sử dụng, chú trọng những thông tin cần thiết.
- Trang web có thiết kế tương thích đa thiết bị -- máy tính và các thiết bị di động (mobile, tablet, PC/Mac)
- Sử dụng những phương pháp thiết kế và công nghệ hiện đại

## Mô tả chức năng {#functions}

### Trang chủ (giới thiệu)

- Có chứa một số hình ảnh bắt mắt về Việt Nam và SaigonStar Travel (images slideshow).
- Hiển thị một số tin tức mới nhất/nổi bật liên quan đến Việt Nam và thị thực.
- Hiển thị các banner của các dịch vụ và trang thông tin liên quan. Các banner này có thể thay đổi được bởi quan trị viên.
- Chú trọng hiển thị liên kết đến trang "gởi đơn xin Visa".

### Trang tin tức (news)

- Tin tức có thể được sắp xếp theo chuyên mục (khuyến mãi, văn hóa & lễ hội, xã hội & chính trị, ...)
- Danh sách chuyên mục tin tức được hiển thị bên phải trang.
- Phần chính của trang sẽ hiển thị danh sách các tin (rút gọn) theo chuyên mục.
- Khi khách bấm (click) vào 1 tiêu đề tin tức, sẽ dẫn đến trang hiển thị tin tức chi tiết đầy đủ.
- Tin tức và chuyên mục có thể được thêm/xóa/sửa trong trang quản trị.

### Trang thông tin

Trang thông tin sẽ bao gồm:

- Danh sách các mục đích xin Visa và hướng dẫn
- Danh sách các phương thức thanh toán và hướng dẫn

#### Các loại mục đích xin Visa

- Du lịch (Tourism)
- Công tác (Business)
- Thăm thân (Friend/family visit)

_Có thể bổ sung thêm_

#### Các phương thức thanh toán (payment methods)

- Paypal (thành viên)
- Credit card (VISA, Mastercard)

### Trang gởi đơn (Apply for Visa)

Bao gồm 3 bước

#### Bước 1: Lựa chọn cơ bản

#### Bước 2: Khai báo thông tin chi tiết

- Tên, giới tính

#### Bước 3: Xác nhận và thanh toán

- Sau khi thanh toán thành công

### Trang dành riêng cho khách hàng theo dõi đơn cấp Visa của mình

- Khách hàng điền vào mã số hóa đơn của mình

### Trang quản trị

- Tin tức: có khả năng thêm/xoá/sửa tin tức và các chuyên mục.
- Ngôn ngữ: có chức năng tự động tạo/xóa/sửa ngôn ngữ mới cho website.

### Các chức năng bổ sung đề nghị

#### Trang hỏi đáp (Q & A)

#### Chức năng hỗ trợ trực tuyến (live chat)

Cung cấp khả năng hỗ trợ trực tuyến tức thì trên website. Ngoài ra quản trị viên còn có thể theo dõi tất cả các khách đang truy cập website tại trang nào và có khả năng chủ động giao tiếp với khách.

## Yêu cầu kỹ thuật {#technical}

Dưới đây là một số yêu cầu kỹ thuật tổng quan, để biết thêm chi tiết vui lòng tham khảo Bảng kế hoạch triển khai.

### Tối ưu hoá

- Có các chức năng tối ưu hoá địa chỉ trang web (Search Engine Friendly URL).
- Tối ưu bộ đệm trình duyệt của khách hàng.
- Có bộ đệm trung gian giữa người dùng cuối và mấy chủ, giúp giảm lượng tải của máy chủ và tăng thời gian truy cập của người dùng.

### Bảo mật

- Mọi kết nối từ người dùng đều sử dụng phương thức kết nối bảo mật HTTPS (HTTP over Secure socket layer).
- Có kế hoạch sao lưu & phục hồi CSDL khách hàng và website nhanh chóng.
- Có các cơ sở bảo mật: Chống DDoS, chống XSS, theo dõi băng thông, ẩn IP máy chủ đối với người dùng cuối.

### Thanh toán trực tuyến

- Tích hợp dịch vụ thanh toán của Paypal (thông qua API).

### Máy chủ email

- Có máy chủ email riêng cho tên miền riêng
- Dung lượng lưu trữ mỗi địa chỉ email là 10 GB
- Số lượng địa chỉ email tối đa là 200 địa chỉ


