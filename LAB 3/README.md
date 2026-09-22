LAB 3 - NHẬN DIỆN VÀ ỨNG PHÓ CÁC MỐI ĐE DỌA ĐẾN AN TOÀN THÔNG TIN



1\. Thông tin sinh viên



\- Họ và tên: Nguyễn Thị Thanh Hiền

\- MSSV: 1150080092

\- Tên Lab: Lab 3 - Nhận diện và ứng phó các mối đe dọa đến an toàn thông tin

\---

2\. Phiên bản môi trường



Môi trường thực hành được triển khai trên máy ảo Windows 11 bằng VMware Workstation.



VMware Workstation Pro 

Hệ điều hành Windows 11 25H2 x64 

OS Build

Microsoft Defender

PowerShell

Sysmon

Autoruns

Process Explorer 

Wireshark 

Python 3.14.7 

Mạng VM, Host-only

\---

3\. Cách dựng môi trường



Bước 1: Chuẩn bị máy ảo



\- Tạo máy ảo Windows 11 25H2 x64 bằng VMware Workstation Pro.

\- Cấu hình tối thiểu:

&#x20; - 2 vCPU

&#x20; - 6 GB RAM

&#x20; - 64 GB ổ đĩa

\- Network Adapter được cấu hình ở chế độ Host-only.

\- Cập nhật Windows theo yêu cầu của bài Lab.

\- Tạo snapshot sạch trước khi thực hành.



Bước 2: Tạo cấu trúc thư mục



Bước 3: Chuẩn bị dữ liệu Lab



\- Sao chép LAB3\_Threats\_Assets.zip vào:



C:\\LAB3\\Downloads



\- Kiểm tra SHA-256 của file.

\- Giải nén dữ liệu vào C:\\LAB3.



Bước 4: Cài đặt công cụ



Các công cụ được sử dụng:



\- Python

\- Wireshark + Npcap

\- Sysmon

\- Autoruns

\- Process Explorer

\- Microsoft Defender

\- Windows Event Viewer



Bước 5: Thu thập Baseline



Trước khi thực hiện các tình huống, tiến hành thu thập trạng thái ban đầu của:



\- Hệ điều hành

\- Microsoft Defender

\- Windows Firewall

\- Cấu hình mạng

\- Các process đang chạy



Các kết quả được lưu trong:



C:\\LAB3\\Evidence



\---



4\. Các tình huống đã thực hiện



&#x20;TH1 - Xác định tài sản, lỗ hổng, mối đe dọa và rủi ro



Nội dung:

\- Xác định các tài sản trên máy ảo.

\- Phân biệt Asset, Vulnerability, Threat, Risk và Control.

\- Xây dựng Risk Register.

\- Phân loại các nguồn đe dọa.



\---



&#x20;TH2 - Mã độc và Microsoft Defender



Nội dung:

\- Kiểm tra trạng thái Microsoft Defender.

\- Sử dụng EICAR Standard Anti-Virus Test File.

\- Quan sát khả năng phát hiện của Microsoft Defender.

\- Kiểm tra Protection History.

\- Thu thập bằng chứng phát hiện EICAR.

\---

5\. Cleanup và phục hồi hệ thống



Sau khi hoàn thành việc thu thập bằng chứng:



\- Xóa LAB3\_Run\_Demo.

\- Xóa LAB3\_Persistence\_Demo.

\- Dừng HTTP Server trên port 8080.

\- Xóa tài khoản lab3user.

\- Kiểm tra lại Microsoft Defender.

\- Thu baseline Autoruns sau cleanup.

\- So sánh trạng thái trước và sau.

\- Tính SHA-256 cho các file bằng chứng.

\- Khôi phục máy ảo về snapshot sạch sau khi hoàn thành Lab.



