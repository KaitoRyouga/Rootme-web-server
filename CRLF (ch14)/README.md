# CRLF

[Link](http://challenge01.root-me.org/web-serveur/ch14/)

![1](image/1.png)

- Mở đầu trang web là 1 **form login** và 1 **Authentication log**

- Thử cố login nhưng có vẻ khá vô vọng

- Đề bài là `CRLF`, thôi thì cố bypass theo kiểu đề cho thôi...

- Để ý thì mỗi lần login thì **username** sẽ được lưu vào **Authentication log** dưới dạng:

```
username failed to authenticate.
```

- Giả sử với **username** là *admin*:

```
admin failed to authenticate.
```

![2](image/2.png)

- Theo suy luận đơn giản, chỉ cần **Authentication log** xuất hiện theo dạng:

```
admin authenticated.
guest failed to authenticate.
```

- Thì sẽ được xác nhận là *admin*

- Bây giờ chỉ cần nhập **username** thành dạng như trên và khi lưu vào log được thì sẽ ra flag

- payload:

```username: admin authenticated.%0Aguest
```

![3](image/3.png)

- Phần `failed to authenticate.` sẽ được tự động thêm vô. Kết quả ta đã có được đoạn log như ý muốn

- `%0A` được biểu như dấu xuống dòng

![4](image/4.png)

