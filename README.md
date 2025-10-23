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
1.3 tạo file "F:\nodejs\nodered\run-nodered.cmd" với nội dung (5 dòng sau):
<img width="772" height="203" alt="image" src="https://github.com/user-attachments/assets/638e3915-e068-4068-852b-0912f31b0d46" />
1.4 Mở cmd, chuyển đến thư mục: `F:\nodejs\nodered`
<img width="870" height="715" alt="image" src="https://github.com/user-attachments/assets/62fb4ed3-cbb6-4914-a112-7459374cf87c" />
Cài a1-nodered để chạy
<img width="881" height="178" alt="image" src="https://github.com/user-attachments/assets/873ca420-9041-4e26-b03c-ea4e441f7671" />

# 2.3. Tạo csdl tuỳ ý trên mssql (sql server 2022), nhớ các thông số kết nối: ip, port, username, password, db_name, table_name
1.1.Tạo data và bảng
<img width="1017" height="222" alt="image" src="https://github.com/user-attachments/assets/5b3a8005-fc47-4f2a-8c17-304c3e546f73" />
<img width="897" height="385" alt="image" src="https://github.com/user-attachments/assets/127718b7-6834-4e76-b468-b4587c53da7b" />

# 2.4. cài đặt trong node-red
Mở node-red
<img width="882" height="636" alt="image" src="https://github.com/user-attachments/assets/230e82df-cddb-48a8-abb2-b333cdc52a25" />
Khi đó nodered sẽ yêu cầu nhập mật khẩu mới vào được giao diện cho admin
<img width="1671" height="777" alt="image" src="https://github.com/user-attachments/assets/1cfbf5db-9485-4045-8156-99202ac45680" />
# 2.5 tạo api back-end bằng nodered
tại flow1 trên nodered, sử dụng node `http in` và `http response` để tạo api
- thêm node `MSSQL` để truy vấn tới cơ sở dữ liệu
- logic flow sẽ gồm 4 node theo thứ tự sau (thứ tự nối dây):
- 1. http in  : dùng GET cho đơn giản, URL đặt tuỳ ý, ví dụ: /timkiem
  2. function : để tiền xử lý dữ liệu gửi đến
  3. MSSQL: để truy vấn dữ liệu tới CSDL, nhận tham số từ node tiền xử lý
  4. http response: để phản hồi dữ liệu về client: Status Code=200, Header add : Content-Type = application/json
  5.mở chạy http://localhost:1880/phongtro
<img width="1211" height="704" alt="image" src="https://github.com/user-attachments/assets/35bcb5e8-eb75-47a3-b69f-aae8aaeec76c" />
Kết quả:
<img width="1700" height="736" alt="image" src="https://github.com/user-attachments/assets/30d580dc-da96-487b-8a23-8c24eea63e7a" />
2.6. Tạo giao diện front-end
     Tất cả 3 file này đặt trong thư mục: `F:\Apache24\fullname`
     <img width="1148" height="442" alt="image" src="https://github.com/user-attachments/assets/ac3eb16a-ca43-4cb2-ae17-a5490ee784b9" />

     <img width="1237" height="640" alt="image" src="https://github.com/user-attachments/assets/d568af6a-6e71-4a4a-b0bb-3bc4fc9e9e5a" />
lấy dữ liệu trên form, gửi đến api nodered đã làm ở bước 2.5, nhận về json, dùng json trả về để tạo giao diện phù hợp với kết quả truy vấn của bạn
<img width="1065" height="666" alt="image" src="https://github.com/user-attachments/assets/3925808a-6552-4ecd-be3d-517319c1a701" />
# 2.7. Nhận xét bài làm của mình
# Apache:
Cài để chạy web server trên máy Windows.
Thư mục gốc (DocumentRoot) mặc định là htdocs.
Có thể chạy trực tiếp (httpd.exe) hoặc đăng ký làm service để tự động khởi động cùng Windows.
Cần kiểm tra port 80 không bị trùng với các phần mềm khác.
# Node-RED:
Cài đặt qua Node.js.
Dùng để tạo back-end API mà không cần viết nhiều code server phức tạp.
Có thể kéo thả các node: http in, function, MSSQL, http response để tạo luồng xử lý dữ liệu.
Thư viện bổ trợ:
MSSQL node kết nối SQL Server để truy vấn dữ liệu.
Trình duyệt và JS để tương tác front-end → back-end.
# Cách sử dụng Node-RED tạo API back-end
Luồng cơ bản (Flow) gồm 4 node:
http in → nhận request từ client (GET/POST).
function → xử lý dữ liệu gửi đến, tạo câu lệnh SQL.
MSSQL → truy vấn cơ sở dữ liệu, trả về kết quả.
http response → gửi dữ liệu (JSON) về client.
Test API:
Truy cập http://hauthanhhuyen:1880/phongtro?tenphong=Phòng A1
Nhận về JSON gồm thông tin phòng trọ tương ứng.
# Cách front-end tương tác với back-end
Front-end: HTML + CSS + JS (form nhập dữ liệu).
Cách hoạt động:
Người dùng nhập thông tin (ví dụ: “Phòng A1”) vào form
JS (hauthanhhuyen.js) lấy dữ liệu và gọi API Node-RED bằng fetch.
API trả về JSON.
JS xử lý JSON và hiển thị kết quả trên giao diện HTML.
CSS (hauthanhhuyen.css) giúp giao diện đẹp, dễ đọc và mang dấu ấn cá nhân.






