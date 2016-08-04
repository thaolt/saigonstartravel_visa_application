# III. Bảng kế hoạch triển khai

## III.1. Triển khai hạ tầng kỹ thuật {#sysspecs}

### III.1.1. Cài đặt hệ thống phần mềm

* Nền tảng ứng dụng: HTML5 Web/Apache2+NGINX
* Cơ sở dữ liệu nền: MySQL 5.5
* Ngôn ngữ lập trình chính: PHP, Javascript
* Mô hình phần mềm: MVC
* Frameworks: Google Material Design, jQuery
* Công nghệ được áp dụng: Ajax, WebSocket

### III.1.2. Triển khai hệ thống mạng máy chủ

* Tích hợp mạng phân bổ nội dung (CDN)
* Triển khai hệ thống cân bằng tải (Load balancer)
* Xin cấp phép và cài đặt chứng thực bảo mật (SSL certificate) cho phép truyền tải nội dung qua giao thức được mã hóa HTTPS
* Triển khai hệ thống máy chủ email (mail server), cài đặt giao tiếp email cho người dùng (webmail)

### III.1.3. Hạ tầng máy chủ đề nghị

* Dung lượng đĩa: 40 GB
* Băng thông mạng: 3000 GB /tháng
* Tốc độ mạng: 1 Gbps
* Hệ điều hành: Debian Linux 8

## III.2. Chuyển giao công nghệ và đào tạo {#tranfer}

* Sau khi nghiệm thu, DFM sẽ gởi một kỹ sư phần mềm đến SaigonStar Travel để tiến hành chuyển giao công nghệ và đào tạo quản trị viên cho SaigonStar Travel.

* Thông tin các loại tài khoản sẽ chuyển giao:
    * Tài khoản quản trị Server lưu trữ.
    * Tài khoản sao lưu trên điện toán đám mây (cloud).
    * Tài khoản quản trị website.
    * Tài khoản quản lý thông tin tên miền.

* Chuyển giao cũng bao gồm các tài liệu:
    * Tài liệu hướng dẫn sử dụng
        * Dành cho quản trị viên.
        * Dành cho nhân viên xử lý đơn xin thị thực.
        * Dành cho nhân viên nhập liệu ( tin tức, thông báo )
    * Tài liệu kỹ thuật
        * Quy trình sao lưu-phục hồi sau sự cố.
        * Tài liệu vận hành máy chủ.
