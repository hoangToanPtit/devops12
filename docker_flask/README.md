Sự khác biệt giữa mạng bridge và mạng bridge do người dùng tự tạo:
1. DNS:
+ Trong mạng mặc định: không có tính năng này -> nên các container phải giao tiếp với nhau thông qua địa chỉ IP
+ Trong mạng tự tạo ra: các container trong cùng một mạng có thể giao tiếp với nhau thông qua 2 cách là: địa chỉ IP hoặc tên miền

2. Cấu hình mạng:
+ Trong mạng mặc đinh: sử dụng các cấu hình mặc định -> không thay đổi được
+ Trong mạng tự tạo: có thể tự cấu hình 

3. Isolation:
+ Mạng mặc đinh: có thể dẫn đến việc các container không liên quan đến nhau cũng có thể giao tiếp với nhau -> ảnh hưởng đến tính bảo mật
+ Mạng do người dùng tạo ra: chỉ những container nằm trong mạng đó mới giao tiếp được với nhau được -> đảm bảo dự liệu được đóng gói, bảo mật

4. Enviroment variables 
+ Mạng mặc định: để chia sẻ biến môi trường bằng cách dùng --link flag
+ Mạng tự tạo ra: không dùng --link flag -> sử dụng một file cấu hình của docker compose để định nghĩa và chia sẻ các biến môi trường

