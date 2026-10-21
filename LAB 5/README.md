
# LAB – CẤU HÌNH VÀ KIỂM THỬ FIREWALL PFSENSE

**1. Thông tin sinh viên**

- **Họ và tên:** Nguyễn Thị Thanh Hiền
- **MSSV:** 1150080092
- **Lớp:** 11_DH_CNPM2
- **LAB 5**: Cấu hình và kiểm thử Firewall pfSense

## 1. Thông tin sinh viên
- **Họ và tên:** Nguyễn Thị Thanh Hiền
- **MSSV:** 1150080092
- **Lớp:** 11CNPM2
- **Môn học:** An toàn thông tin

**2. Mục tiêu bài lab**

Các nội dung thực hiện:

- Cài đặt và cấu hình pfSense.
- Thiết lập hệ thống mạng WAN, LAN và DMZ.
- Cấu hình Windows Server làm Domain Controller và DNS Server.
- Cài đặt IIS Web Server trong vùng DMZ.
- Cấu hình Outbound NAT để các máy trong LAN truy cập Internet.
- Thiết lập và kiểm thử các Firewall Rule.
- Kiểm tra khả năng cho phép hoặc chặn lưu lượng mạng.
- Thực hiện các tình huống kiểm thử chính sách bảo mật.

## 2. Môi trường thực hiện
- VMware Workstation
- pfSense CE
- Windows Server (Domain Controller, DNS Server)
- Windows Server (DMZ-Web)
- PowerShell/CMD và trình duyệt Web

## 3. Nội dung thực hiện
- Cấu hình interface LAN trên pfSense.
- Cài đặt Active Directory Domain Services và tạo Domain Controller.
- Cấu hình DNS Forwarder và kiểm tra phân giải tên miền.
- Truy cập WebGUI pfSense tại `https://10.0.0.1`.
- Cấu hình interface DMZ với IP `172.16.0.1/16`.
- Tạo máy DMZ-Web với IP `172.16.0.2/16`.
- Kiểm tra Outbound NAT và chuẩn hóa Firewall Rules LAN.
- Kiểm tra kết nối khi bật/tắt rule LAN.
- Thực hiện Tình huống 1: chặn ICMP nhưng vẫn cho phép DNS và HTTP/HTTPS.

## 4. Kết quả
- Cấu hình LAN, Domain Controller và DNS.
- Truy cập được giao diện quản trị pfSense.
- Thiết lập vùng DMZ và máy chủ DMZ-Web.
- Kiểm tra rule LAN ở trạng thái bật/tắt.
- Thực hiện kiểm thử chặn ICMP và kiểm tra DNS, HTTP/HTTPS.

## 5. Kết luận
Đã thực hiện các bước cấu hình mạng LAN, Domain Controller, DNS, DMZ và Firewall Rules trên pfSense. Báo cáo có ghi nhận các bước kiểm tra kết nối và thực hiện Tình huống 1.
