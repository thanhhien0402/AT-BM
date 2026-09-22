LAB 1: BẮT GÓI TIN TELNET - SSH



1\. Thông tin sinh viên



\- Họ và tên: Nguyễn Thị Thanh Hiền

\- MSSV: 1150080092

\- Tên bài Lab: Lab 1 - Bắt gói tin Telnet - SSH



2\. Mục tiêu



Bài Lab nhằm tìm hiểu cách thức hoạt động của hai giao thức Telnet và SSH trong quá trình kết nối từ xa giữa Client và Server. Đồng thời sử dụng Wireshark để bắt và phân tích các gói tin được trao đổi trong quá trình kết nối. Thông qua kết quả thực hành, tiến hành so sánh sự khác nhau giữa Telnet và SSH, đặc biệt về khả năng bảo vệ dữ liệu trong quá trình truyền.



3\. Môi trường thực hiện



\- Phần mềm ảo hóa: VMware Workstation

\- Server: Ubuntu Server

\- Client: Windows 11

\- Công cụ:

&#x20; - Wireshark

&#x20; - PuTTY

&#x20; - Telnet Server

&#x20; - OpenSSH Server

4\. Nội dung đã thực hiện



\- Thiết lập môi trường Client/Server.

\- Kiểm tra kết nối mạng giữa Client và Server.

\- Cấu hình dịch vụ Telnet trên Server.

\- Kết nối từ Client đến Server bằng Telnet.

\- Sử dụng Wireshark để bắt và phân tích lưu lượng Telnet.

\- Thử nghiệm Telnet với mật khẩu có độ phức tạp cao hơn.

\- Cấu hình dịch vụ SSH trên Server.

\- Kết nối từ Client đến Server bằng SSH.

\- Sử dụng Wireshark để bắt và phân tích lưu lượng SSH.

\- So sánh dữ liệu thu được giữa phiên Telnet và phiên SSH.



5\. Kết quả thực hiện



\- Thiết lập môi trường mạng Client/Server: \[PASS/FAIL]

\- Kết nối Telnet: \[PASS/FAIL]

\- Bắt và phân tích gói tin Telnet: \[PASS/FAIL]

\- Kết nối SSH: \[PASS/FAIL]

\- Bắt và phân tích gói tin SSH: \[PASS/FAIL]



Qua quá trình thực hành có thể quan sát được sự khác biệt giữa Telnet và SSH khi phân tích bằng Wireshark.



Đối với Telnet, dữ liệu của phiên làm việc có thể xuất hiện ở dạng đọc được khi bắt đúng lưu lượng. Việc sử dụng mật khẩu phức tạp không làm cho kênh truyền Telnet được mã hóa.



Đối với SSH, Wireshark vẫn có thể quan sát các thông tin của kết nối như địa chỉ IP, cổng, thời gian và kích thước gói tin, tuy nhiên nội dung của phiên làm việc được mã hóa nên không thể đọc plaintext giống như Telnet.

