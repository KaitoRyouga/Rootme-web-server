# File upload - MIME type

[Link](http://challenge01.root-me.org/web-serveur/ch21/)

- Trang web tựa như bài `File upload - Double extensions`, upload cũng như vậy. Nhưng có vẻ kỹ thuật này bị fail rồi, ta không thể **injection** vào server thông qua file vừa up

![1](image/1.png)

![2](image/2.png)

![3](image/3.png)

![4](image/4.png)

![5](image/5.png)

![6](image/6.png)

- Có vẻ như bài này nhận diện file thông qua client, thử dùng `Burp suite` để chặn lại rồi đôi **type** xem sao

![7](image/7.png)

- Sửa `Content-Type: application/x-php` thành `Content-Type: image/png`

![8](image/8.png)

![9](image/9.png)

- OK, thành công như ý muốn

![10](image/10.png)

- Các bước còn lại làm như bài `File upload - Double extensions`

- Payload:

```
cat ../../../.passwd
```

![11](image/11.png)
