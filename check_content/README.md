Sự khác biệt giữa ENTRYPOINT và CMD
1. ENTRYPOINT
+ ENTRYPOINT định nghĩa một lệnh mặc định sẽ được thực thi khi khởi chạy container
+ Khi chạy lệnh docker run image_name agrs -> agrs là các đối số được truyền vào cho lệnh ở entrypoint
+ ENTRYPOINT không bị ghi đè khi chạy container -> muốn ghi đè thì phải dùng --entrypoint "new_entrypoint"
2. CMD
+ Định nghĩa: 
	Khi không có ENTRYPOINT: CMD đĩnh nghĩa một lệnh với đầy đủ tham số mặc định, 
	Khi có EWNTRYPOIN: CMD định nghĩa các tham số mặc định cho lệnh được định nghĩa trong ENTRYPOIN
+ CMD bị ghi đè nếu nếu truyền các đối số vào lệnh docker run
3. Best practices:
+ Sử dung ENTRYPOINT đề định nghĩa lệnh mặc định khi khởi chạy ứng dụng
+ Và sử dụng CMD là đối só mặc định cho ENTRYPOINT
