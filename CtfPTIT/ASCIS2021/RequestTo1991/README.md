![image](https://user-images.githubusercontent.com/48151790/132658509-b137df7f-57f2-4caf-9c40-6ad80dbca2f1.png)

Hic server bài này đóng mất rồi nên không có ảnh chụp cụ thể :(

- Dùng dirsearch để xem thư mục ẩn =› ta tìm được /robots.txt/

- Trong file này ta sẽ được gợi ý 2 file khác là debug.aspx và a_d_m_i_n.aspx

- Thử vào 2 file này ta sẽ không thu được gì cả.

- Dựa vào gợi ý của đề bài "How to request back to 1991s?"

- Đặt ra câu hỏi làm sao để gửi request trong nhũng năm 1991?

- Tra GG thu được các thông tin như: những năm 1991 thì giao thức được dùng là HTTP 0.9

- Vậy HTTP 0.9 là gì? Và được sử dụng như thế nào?

![image](https://user-images.githubusercontent.com/48151790/132660208-edafdbd5-3105-4bf8-9c99-a6c564955cb7.png)

Đến đây bài này có 2 cách làm.

Cách 1: Sử dụng telnet kết  đến server sau đó gửi request "GET /a_d_m_i_n.aspx" =› Thu được Flag

Cách 2: File a_d_m_i_n.aspx có gợi ý là "if you are Smuggler"

  =› Ta có thể lợi dụng lỗ hổng HTTP Request Smuggling để khai thác
  
  + Bước 1: Sử dụng BurpSuite để bắt request 
  
  + Bước 2: Bỏ trường Connection: Close
  
  + Bước 3: Thêm request "GET /a_d_m_i_n.aspx" vào bên dưới request bắt được 
  
  + Bước 4: Thay đổi Conntent-Length sao sao cho bao gồm cả request mới, tắt chế độ auto update request của Burp Suite
  
  =›Thu được Flag
