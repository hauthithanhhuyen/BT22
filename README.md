# BT22
HAU THANH HUYEN
# Cài đặt Apache web server:
- Vô hiệu hoá IIS: nếu iis đang chạy thì mở cmd quyền admin để chạy lệnh: iisreset /stop
<img width="765" height="148" alt="image" src="https://github.com/user-attachments/assets/92740df5-bb11-4a5a-b365-e8530ec5061e" />
Download apache server, giải nén ra ổ D
<img width="1199" height="242" alt="image" src="https://github.com/user-attachments/assets/a7853964-66a1-44e1-9aab-95382959b795" />
 giải nén ra ổ f
<img width="944" height="477" alt="image" src="https://github.com/user-attachments/assets/db4ee49f-c4dd-4665-bc59-75b0c970d17a" />
Cấu hình file httpd.conf
<img width="537" height="168" alt="image" src="https://github.com/user-attachments/assets/c2a1c6b9-d672-4b1b-946b-3a10ae3fd490" />
Bước 1 — Đặt thư mục gốc cho website sửa lại thành:
<img width="939" height="189" alt="image" src="https://github.com/user-attachments/assets/56dff0b1-91ee-4dc0-b22f-ca09070cdc6d" />
Bước 2 — Bật VirtualHost
Bỏ dấu # để kích hoạt
<img width="537" height="168" alt="image" src="https://github.com/user-attachments/assets/93cb502c-83f5-4d82-a608-886f4dcf133c" />
Bước 3. Cấu hình file httpd-vhosts.conf
<img width="860" height="325" alt="image" src="https://github.com/user-attachments/assets/776b4a90-abcb-4266-ac8a-65feb1ea79cf" />
Bước 4. Tạo thư mục chứa website
<img width="1027" height="304" alt="image" src="https://github.com/user-attachments/assets/cd327ef4-5386-40cc-9373-09d6c5d4564a" />
B5. Thao tác dòng lệnh trên file `D:\Apache24\bin\httpd.exe` với các tham số `-k install` và `-k start` để cài đặt và khởi động web server apache.
<img width="701" height="184" alt="image" src="https://github.com/user-attachments/assets/ebc61e5e-4d36-401a-85ce-8812ffa248fb" />
Chạy thành công
<img width="832" height="364" alt="image" src="https://github.com/user-attachments/assets/91a6a73d-9116-4a59-bdb8-e5dfb73da033" />
# 2.2. Cài đặt nodejs và nodered => Dùng làm backend:
1.1 Tải bản Node.js
<img width="736" height="166" alt="image" src="https://github.com/user-attachments/assets/def8ed8c-268d-4221-9f99-8aa3b32756d6" />
1.2. Cài đặt 
<img width="849" height="201" alt="image" src="https://github.com/user-attachments/assets/f215f1d3-d755-4acd-bdc5-564709b5dbd4" />
1.3 tạo file "D:\nodejs\nodered\run-nodered.cmd" với nội dung (5 dòng sau):
<img width="772" height="203" alt="image" src="https://github.com/user-attachments/assets/638e3915-e068-4068-852b-0912f31b0d46" />
1.4 Mở cmd, chuyển đến thư mục: `D:\nodejs\nodered`
<img width="870" height="715" alt="image" src="https://github.com/user-attachments/assets/62fb4ed3-cbb6-4914-a112-7459374cf87c" />
Cài a1-nodered để chạy
<img width="881" height="178" alt="image" src="https://github.com/user-attachments/assets/873ca420-9041-4e26-b03c-ea4e441f7671" />

# 2.3. Tạo csdl tuỳ ý trên mssql (sql server 2022), nhớ các thông số kết nối: ip, port, username, password, db_name, table_name
1.1.Tạo data và bảng
<img width="1017" height="222" alt="image" src="https://github.com/user-attachments/assets/5b3a8005-fc47-4f2a-8c17-304c3e546f73" />
1.2 cài đặt trong node-red
Mở node-red
<img width="882" height="636" alt="image" src="https://github.com/user-attachments/assets/230e82df-cddb-48a8-abb2-b333cdc52a25" />
1.3 





