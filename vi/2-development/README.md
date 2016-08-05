# II. Thiết kế & Xây dựng website SaigonStar Travel

## II.1. Yêu cầu tổng quan {#overview}

Công ty SaigonStar Travel muốn có một giải pháp cho phép người sử dụng có thể gởi yêu cầu đăng ký Visa đến Việt Nam trực tuyến và nhận phản hồi qua email thông qua dịch vụ web của công ty. Khách hàng có thể thanh toán phí dịch vụ trực tiếp trên website của SaigonStar Travel.

### II.1.1. Mục tiêu

* Khách quan tâm có thể thăm trang web và xem danh sách các loại đơn xin Visa với các mục đích khác nhau như: du lịch, công tác, thăm thân, v.v..
* Khách hàng có thể gởi đơn yêu cầu xin Visa trực tiếp trên trang web.
* Cho phép thanh toán trực tuyến \( đối tượng khách hàng khách Châu Âu đang muốn đến Việt Nam \).
* Có kế hoạch marketing trực tuyến cho website giúp đến gần với đối tượng khách hàng tiềm năng.
* Tích hợp sẵn 4 ngôn ngữ: Anh, Pháp, Đức, Tây Ban Nha \( cho phép quản trị viên tự thêm và sửa đổi ngôn ngữ \).
* Trang web phải có bảo mật và độ an toàn dữ liệu cao.
* Có sử dụng công cụ theo dõi và báo cáo tình trạng khách viếng thăm website \(Google Analytics\).

### II.1.2. Yêu cầu thiết kế

* Có giao diện được thiết kế sáng sủa đơn giản dễ sử dụng, chú trọng những thông tin cần thiết.
* Trang web có thiết kế tương thích đa thiết bị -- máy tính và các thiết bị di động \(mobile, tablet, PC\/Mac\).

![](/assets/responsive.png)

* Sử dụng những phương pháp thiết kế và công nghệ hiện đại.

## II.2. Mô tả công việc thiết kế và xây dựng {#functions}

### II.2.1. Trang chủ \(giới thiệu\)

* Có chứa một số hình ảnh bắt mắt về Việt Nam và SaigonStarTravel \(images slideshow\).
* Hiển thị một số tin tức mới nhất\/nổi bật liên quan đến Việt Nam và thị thực.
* Hiển thị các banner của các dịch vụ và trang thông tin liên quan. Các banner này có thể thay đổi được bởi quan trị viên.
* Chú trọng hiển thị liên kết đến trang "gởi đơn xin Visa".

### II.2.2. Trang tin tức \(news\)

* Tin tức có thể được sắp xếp theo chuyên mục \(khuyến mãi, văn hóa & lễ hội, xã hội & chính trị, ...\)
* Danh sách chuyên mục tin tức được hiển thị bên phải trang.
* Phần chính của trang sẽ hiển thị danh sách các tin \(rút gọn\) theo chuyên mục.
* Khi khách bấm \(click\) vào 1 tiêu đề tin tức, sẽ dẫn đến trang hiển thị tin tức chi tiết đầy đủ.
* Tin tức và chuyên mục có thể được thêm\/xóa\/sửa trong trang quản trị.

### II.2.3. Trang thông tin \(information\)

Trang thông tin sẽ bao gồm:

* Danh sách các mục đích xin Visa và hướng dẫn.
* Danh sách các phương thức thanh toán và hướng dẫn.

* **Các trang con của các loại mục đích xin Visa**

  * Du lịch \(Tourism\)
  * Công tác \(Business\)
  * Thăm thân \(Friend\/family visit\)

    _Có thể bổ sung thêm_



* **Danh sách các phương thức thanh toán \(payment methods\)**

  * Paypal \(cho khách hàng có tài khoản Paypal\)
  * Stripe Credit card processor \(VISA, Mastercard, JCB\)


_Lưu ý: **Stripe** lấy phí dịch vụ trên mỗi giao dịch là _****_2,9% + 30cents_****_. Ví dụ: với 1 giao dịch trị giá 15 US$ thì phí dịch vụ của Stripe là 30,435. Giá trị nhận được của giao dịch đó là khoảng 14.69 US$._

_Phí dịch vụ của **PayPal** là **4.4% + 30cents.**_


### II.2.4. Trang gởi đơn \(Apply for Visa\)

Trang này sẽ tính và hiển thị tức thời số phí dịch vụ mà khách hàng cần phải trả phản ánh lựa chọn của khách hàng.

Bao gồm 3 bước như sau:

* **Bước 1: Các lựa chọn cơ bản**

Đây là nội dung đề nghị, có thể sửa đổi tuỳ theo yêu cầu của quý khách hàng.

Khách sẽ lựa chọn các tuỳ chọn bao gồm:

  * Số lượng Visa muốn xin ( vd: 1-20 ứng viên )
  * Thời gian xin phép, vd:

    * 1 người: 1 - 3 tháng
    * Nhiều người: 1 - 6 tháng

  * Mục đích viếng thăm

      * Du lịch
      * Công tác
      * Thăm thân

  * Sân bay đến, bao gồm 

      * Nội Bài
      * Tân Sơn Nhất
      * Đà Nẵng
      * Cam Ranh

  * Dịch vụ cộng thêm ( có tính thêm phí cho khách hàng )

      * Dịch vụ làm thủ tục nhập cảnh tại sân bây
      * Dịch vụ gọi xe

* **Bước 2: Khai báo thông tin chi tiết**

Khách hàng sẽ điền vào Form thông tin chi tiết cho từng ứng xin cấp thị thực, bao gồm các thông tin:

  * Tên đầy đủ
  * Ngày tháng năm sinh, nơi sinh
  * Quốc tịch
  * Nghề nghiệp
  * Địa chỉ hiện tại
  * Thông tin hộ chiếu ( tên trên hộ chiếu, loại hộ chiếu, cấp bởi, ngày cấp, ngày hết hạn )
  * Ngày nhập cảnh dự kiến
  * Ngày xuất cảnh
  * Đã từng đến Việt Nam hay chưa?
  * Upload hình chụp hoặc scan của hộ chiếu (2 mặt)

* **Bước 3: Xác nhận và thanh toán**

    * Website sẽ cho phép khách hàng lựa chọn phương thức thanh toán.
    * Sau khi lựa chọn phương thức thanh toán, khách hàng sẽ điền vào thông tin thanh toán của mình ( vd: số thẻ Credit card, tên trên thẻ, địa chỉ thanh toán, CVV ).
    * Website sẽ liên kết với các cổng thanh toán (Paypal, Stripe) để xác nhận nếu thanh toán thành công sẽ hiển thị mã số theo dõi cho khách hàng và thông điệp cảm ơn.


### II.2.5. Trang dành riêng cho khách hàng theo dõi đơn cấp Visa của mình

* Khách hàng điền vào mã số theo dõi của mình. Website sẽ hiển thị tình trạng đơn xin cấp thị thực của khách hàng. Có các tình trạng như sau: đã gởi đến SaigonStarTravel, đã gởi đến Cục Quản lý Xuất nhập cảnh, đã có văn bản xác nhận.

### II.2.6. Trang quản trị

* Trang chủ: có thể thay đổi cách hiển thị các module và slideshow trên trang chủ
* Quản lý nội dung
    * Tin tức: có khả năng thêm\/xoá\/sửa tin tức và các chuyên mục.
    * Thêm/xoá/sửa nội dung các trang thông tin

* Quản lý đơn xin cấp phép ( xem, tải các thông tin chi tiết của đơn xin thị thực, cập nhật tình trạng ). Tự động gởi mail cho khách hàng khi tình trạng đơn được thay đổi.
* Quản lý khách hàng: Liệt kê khách hàng và đơn xin cấp phép của họ. Gởi email trực tiếp cho khách hàng.
* Ngôn ngữ: có chức năng tự động tạo\/xóa\/sửa ngôn ngữ mới cho website.


### II.2.7. Các chức năng bổ sung đề nghị

* **Trang hỏi đáp \(Q & A\)**

  * hỏi đáp


* **Chức năng hỗ trợ trực tuyến \(live chat\)**

  * Cung cấp khả năng hỗ trợ trực tuyến tức thì trên website. Ngoài ra quản trị viên còn có thể theo dõi tất cả các khách đang truy cập website tại trang nào và có khả năng chủ động giao tiếp với khách.


## II.3. Triển khai hạ tầng kỹ thuật {#technical}

Dưới đây là một số yêu cầu kỹ thuật tổng quan, để biết thêm chi tiết vui lòng tham khảo Bảng kế hoạch triển khai.

### II.3.1 Tối ưu hoá website

* Có các chức năng tối ưu hoá địa chỉ trang web \(Search Engine Friendly URL\).
* Tối ưu bộ đệm trình duyệt của khách hàng.
* Có bộ đệm trung gian giữa người dùng cuối và mấy chủ, giúp giảm lượng tải của máy chủ và tăng thời gian truy cập của người dùng.

### II.3.2. Xây dựng hệ thống bảo mật

* Mọi kết nối từ người dùng đều sử dụng phương thức kết nối bảo mật HTTPS \(HTTP over Secure socket layer\).
* Có kế hoạch sao lưu & phục hồi CSDL khách hàng và website nhanh chóng.
* Có các cơ sở bảo mật: Chống DDoS, chống XSS, theo dõi băng thông, ẩn IP máy chủ đối với người dùng cuối.

### II.3.3. Tích hợp thanh toán trực tuyến

* Tích hợp dịch vụ thanh toán của Paypal \(thông qua API\).
* Tích hợp dịch vụ thanh toán của Stripe \(thông qua API\).

### II.3.4. Máy chủ email

* Có máy chủ email riêng cho tên miền riêng.
* Dung lượng lưu trữ cho mỗi địa chỉ email là 10 GB.
* Số lượng địa chỉ email tối đa là 200 địa chỉ.

