# HTTP - Directory indexing

[Link](http://challenge01.root-me.org/web-serveur/ch4/)

![home](image/home.png)

- Vừa vào thì chả có gì ở trang web cả, thôi thì `Ctrl + U` Thử xem có gì nào

![u](image/u.png)

- 1 đoạn `include("admin/pass.html")` hiện ngay trước mặt. Cộng thêm tên đề bài `Directory indexing`. Chắc kèo dính lỗi `directory traversal` rồi.

- Tìm hiểu thêm về lỗi này: [Link](https://www.google.com/amp/s/securitydaily.net/tan-cong-directory-traversal-la-gi/amp/)


- Nói sơ lược thì lỗi này là do dev không chặn truy cập folder hay file trái phép từ bên ngoài nên bây giờ ta vô file `admin/pass.html` mà bài cho xem có gì nào

![troll](image/troll.png)

- Nhìn không thấy flag đâu, đọc đoạn thông báo thì có vẻ đây là troll

- thôi thì vô hẳn folder `admin` xem có gì nào

![admin](image/admin.png)

- Nãy vô `pass.html` rồi, giờ vô thử folder `backup` xem sao

![bac](image/bac.png)

- Thấy file `admin.txt`, mở luôn thử

![flag](image/flag.png)

- Flag đây, rồi
