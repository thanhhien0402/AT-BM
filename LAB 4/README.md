# LAB 4 – KHẢO SÁT VÀ ĐÁNH GIÁ BỀ MẶT MẠNG BẰNG NMAP

**1. Thông tin sinh viên**

- Họ và tên: Nguyễn Thị Thanh Hiền 
- MSSV: 1150080092
- Môn học: An toàn hệ thống thông tin
- Tên bài Lab: Lab 4 – Khảo sát và đánh giá bề mặt mạng bằng Nmap

**2. Mục tiêu bài Lab**

Bài Lab nhằm làm quen với công cụ Nmap và sử dụng Nmap để khảo sát, đánh giá bề mặt mạng trong môi trường thực hành cô lập.

Các nội dung chính đã thực hiện:

- Xây dựng môi trường mạng thực hành bằng máy ảo.
- Xác định địa chỉ IP của các máy trong mạng.
- Phát hiện các host đang hoạt động.
- Khảo sát các cổng TCP và UDP.
- So sánh một số kỹ thuật quét TCP.
- Nhận diện dịch vụ và phiên bản dịch vụ.
- Nhận diện hệ điều hành của máy đích.
- Sử dụng NSE để thu thập thông tin SMB và kiểm tra dấu hiệu lỗ hổng MS17-010.
- Xuất kết quả quét ra các định dạng khác nhau.
- Đánh giá sự thay đổi trước và sau khi áp dụng biện pháp hardening.

---

**3. Môi trường thực hành**

Môi trường được triển khai bằng các máy ảo và được cô lập trong cùng mạng nội bộ.

### Các máy sử dụng

| Máy | Vai trò |
|---|---|
| Windows 11 VM | Máy Windows dùng để cài Nmap/Zenmap và làm máy đích đối chiếu |
| Kali Linux VM | Máy quét chính sử dụng Nmap |
| Metasploitable 2 | Máy đích cố ý có các dịch vụ và lỗ hổng phục vụ thực hành |

### Địa chỉ IP sử dụng

| Máy | Địa chỉ IP |
|---|---|
| Kali Linux | ................................ |
| Metasploitable 2 | 192.168.157.129 |
| Windows 11 VM | 192.168.157.130 |

Các máy được cấu hình trong cùng mạng cô lập để có thể giao tiếp với nhau trong quá trình thực hành.

**4. Nội dung đã thực hiện**
- Kiểm tra kết nối giữa Kali và Metasploitable 2; phát hiện các host đang hoạt động.
- Thực hiện TCP Connect (-sT), SYN (-sS), FIN (-sF), Xmas (-sX), NULL (-sN) và ACK (-sA) scan.
- Quét UDP có kiểm soát.
- Nhận diện dịch vụ/phiên bản (-sV), hệ điều hành (-O) và thực hiện Aggressive scan (-A).
- Dùng NSE thu thập thông tin SMB và kiểm tra dấu hiệu MS17-010 trên Metasploitable 2; kiểm tra Windows 11 VM.
- Xuất kết quả Nmap dạng TXT, XML và grepable.

**5. Kết quả chính**
- Metasploitable 2: phát hiện 23 cổng TCP open và 977 cổng closed trong 1.000 cổng mặc định; có các dịch vụ như FTP, SSH, Telnet, HTTP, SMB, MySQL và PostgreSQL.
- UDP: phát hiện 53/udp và 137/udp là open; 67/udp là open|filtered.
- Nhận diện hệ điều hành mục tiêu là Linux 2.6.x.
- SMB trên Metasploitable 2: 445/tcp open; smb-os-discovery nhận diện Unix (Samba 3.0.20-Debian), tên máy metasploitable, domain localdomain. Script smb-vuln-ms17-010 không trả về VULNERABLE, nên chưa đủ bằng chứng kết luận mục tiêu bị ảnh hưởng bởi MS17-010.
- Windows 11 VM: 445/tcp filtered; các script SMB không thu thập được thông tin, nên không thể kết luận tình trạng MS17-010 từ kết quả này.

**6. Kết luận**
Đã sử dụng Nmap để khảo sát host, cổng TCP/UDP, dịch vụ, hệ điều hành và thông tin SMB trong môi trường máy ảo. Kết quả cho thấy Metasploitable 2 có nhiều dịch vụ mở cần được rà soát và giới hạn truy cập; Windows 11 VM lọc cổng SMB 445 trong lần kiểm tra. Không kết luận trạng thái MS17-010 khi script không cung cấp đủ bằng chứng.
