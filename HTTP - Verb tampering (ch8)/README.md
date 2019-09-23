# HTTP - Verb tampering

[Link](http://challenge01.root-me.org/web-serveur/ch8/)

- Bổ trợ kiến thức về lỗi `Verb tampering` và 1 chút CURL trước khi đọc

![home](image/home.png)

- Mở đầu trang web là xác thực tài khoản

- Cố login vào nhưng không được. Để ý laị tên đề `Verb tampering`. Đúng chất cái tên nói lên tất cả. Thử vào curl load trang với `mothod` khác xem

- Sau 1 vài lần thử thì cũng có kết quả

- Payload: 

```
curl -X OPTIONS http://challenge01.root-me.org/web-serveur/ch8/
```

- `CURL -X OPTIONS` ở đây với `-X OPTIONS` là loại method

![flag](image/flag.png)
