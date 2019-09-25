# HTTP - User-agent 

[Link](http://challenge01.root-me.org/web-serveur/ch2/)

- Vừa vào trang web thì có đúng 1 dòng thông báo: 
```
Wrong user-agent: you are not the "admin" browser!
```

![no](image/noi.png)

- Nhìn qua thì có vẻ liên quan tới `Requests Header`

- Đọc thêm về `HTTP Requests` và `HTTP Response` [Link](https://freetuts.net/header-request-va-header-response-670.html)

- Thử vào `Burp suite` sửa đoạn `User-Agent` với value là `admin` xem sao

![admin](image/admin.png)

- Không bất ngờ lắm, flag hiện ra luôn

![flag](image/flag.png)
