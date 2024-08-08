## Git và Github cho sysadmin

### Mục lục

[I. Mở đầu](#Modau)

[II. Ngôn ngữ Markdown](#ngonngumarkdown)

- [1.Tiêu đề cấp 1](#1tiêu-đề-cấp-1)
  - [2.Tiêu đề cấp 2](#2tiêu-đề-cấp-2)
          - [6.Tiêu đề cấp 6](#6tiêu-đề-cấp-6)
    - [2. Chèn link, chèn ảnh](#2-chèn-link-chèn-ảnh)
    - [3. Ký tự in đậm, in nghiêng](#3-ký-tự-in-đậm-in-nghiêng)
    - [4. Trích dẫn, bo chữ](#4-trích-dẫn-bo-chữ)
    - [5. Gạch đầu dòng](#5-gạch-đầu-dòng)
    - [6. Tạo bảng](#6-tạo-bảng)

[Tổng kết](#Tongket)

===========================

<a name="Modau"></a>

## I. Mở đầu

`Git` là một phần mềm dùng để quản lý phiên bản của mã nguồn tương tự như `SVN` nhưng có nhiều ưu điểm hơn, `Git` đang được sủ dụng rộng rãi hiện nay.
Tuy nhiên trong bài viết này, tôi sẽ nói về git một cách "cá nhân" hơn, mang tính chia sẻ những cái tôi hay làm và hướng tới những người là sysadmin. Mong nhận được ý kiến đóng góp của các bạn.

#### Một số khái niệm cần làm rõ

**`Git` và `Github` khác nhau như thế nào?**

Lấy ví dụ, bạn có một đoạn script dài 20 dòng, hôm sau bạn tối ưu nó đi, chỉ còn 15 dòng, một ngày khác bạn sửa ở script đó một vài chỗ. Git ghi lại những thời điểm thay đổi đó của bạn và source code của bạn tại thời điểm đó.

Github là một trang web, cho phép bạn lưu source code của mình lên đó. Sự kết hợp hoàn hảo giữa Git và Github mang lại một sự thuận tiện không hề nhỏ cho người dùng. Bạn có thể thay đổi đoạn code của mình mọi lúc mọi nơi mà không sợ bị ghi đè lên hay bị mất dữ liệu do hỏng hóc vì dữ liệu của bạn được lưu cả trên trang web Github và máy cá nhân. Bạn cũng có thể khôi phục được code của mình về một thời điểm bất kỳ nào đó.

Github có bản free và mất phí. Với Github free thì source code của bạn sẽ công khai, có nghĩa là ai cũng có thể xem code của bạn. Nó phù hợp với các phần mềm nguồn mở, và cũng có thể trở thành một blog cá nhân của chính các bạn như các trang blogspot, wordpress,...

Muốn có thể tạo một kho code bí mật của riêng mình thì bạn phải trả phí.

Đối với cá nhân tôi thì github free là quá đủ cho mục đích lưu trữ và chia sẻ thông tin.

**Cần phải làm gì để có thể sử dụng `Github`?**

- B1: Đăng ký một tài khoản tại [github](https://github.com) và đăng nhập

Tôi chắc chắn rằng một khi bạn đã đọc đến đây thì bạn đã biết thực hiện bước trên như thế nào :)

- B2: Học cách sử dụng ngôn ngữ `Markdown`

Bạn có thể bỏ qua bước này nếu bạn đã biết hoặc các bạn xác định không sử dụng nó để viết.

Theo cá nhân tôi thì các bạn nên viết bằng Markdown trong Github vì nó sẽ mang lại sự tường minh cho bài viết của bạn.

Bạn chỉ cần bỏ ra khoảng 2h là đã có thể sử dụng ngôn ngữ này như ý muốn.

- B3: Tạo một repo đầu tiên và gõ Hello world bằng Markdown

Sau đó tạo các repo tùy mục đích, clone nó về client và code.

Bước này tôi sẽ hướng dẫn chi tiết hơn ở phần sau.

<a name="ngonngumarkdown"></a>

## II. Ngôn ngữ Markdown

Ngôn ngữ này khá đơn giản, bạn có thể đọc tại [đây](http://daringfireball.net/projects/markdown/syntax) để biết cách sử dụng.

Nhưng với tôi, tôi không dùng hết từng ấy thứ cho nên tôi chỉ nhớ một số cái tôi hay dùng, cách tôi dùng như sau:

Tạo một file có tên bất kỳ với đuôi .md. Có thể dùng `notepad`, `notepad++`, `vi`, `nano`,... hay bất cứ thứ gì mà bạn muốn.

Một số phương pháp tôi hay sử dụng để viết:

<a name="thetieude"></a>

### 1. Thẻ tiêu đề

Markdown sử dụng kí tự # để bắt đầu cho các thẻ tiêu đề, có thể dùng từ 1 đến 6 ký tự # liên tiếp. Mức độ riêu đề giảm dần từ 1 đến 6

Tùy mục đích và ý thích bạn có thể sử dụng cách này để thể hiện các chỉ mục khác nhau.

Ví dụ:

```
# 1.Tiêu đề cấp 1
```

# 1.Tiêu đề cấp 1

```
## 2.Tiêu đề cấp 2
```

## 2.Tiêu đề cấp 2

```
###### 6.Tiêu đề cấp 6
```

###### 6.Tiêu đề cấp 6

<a name="chenlinkchenanh"></a>

### 2. Chèn link, chèn ảnh

Để chèn hyperlink bạn chỉ cần paste luôn linh đó vào file .md

```
https://github.com
```

https://github.com

Hoặc bạn cũng có thể sử dụng cú pháp sau để thu ngắn đường dẫn của link

```
[Github](https://github.com)
```

Kết quả là:

[Github](https://github.com)

Để chèn ảnh thì bạn hãy sử dụng cú pháp sau:

```
<img src="link_anh_cua_ban">
```

Tôi thường sử dụng công cụ [Lightshot](https://app.prntscr.com/en/index.html) để chụp ảnh màn hình và up hình đó lên trang http://i.imgur.com/ để lấy đường dẫn ảnh đưa vào Github

Hai công cụ này khá dễ sử dụng, bạn chỉ cần chụp màn hình bằng Lightshot ấn Ctrl + C để copy và Ctrl + V để paste vào trình duyệt tại trang web http://i.imgur.com/

<a name=kytuindaminnghieng></a>

### 3. Ký tự in đậm, in nghiêng

- Để in đậm một đoạn text bạn chỉ cần làm như sau:

```
**từ cần in đậm**
```

**từ cần in đậm**

- Để in nghiên một đoạn text bạn chỉ cần làm như sau:

```
*từ cần in nghiêng*
```

_từ cần in nghiêng_

<a name="trichdanbochu"></a>

### 4. Trích dẫn, bo chữ

Để bo một đoạn text thì bạn chỉ cần sử dụng cú pháp sau:

```
`đoạn cần bo`
```

Kết quả là: `đoạn cần bo`

Để làm nổi bật một đoạn, chẳng hạn như một đoạn shell hay file cấu hình bạn có thể sử dụng cú pháp như ví dụ sau:

    ```sh
    auto eth0
    iface eth0 inet static
    ipaddress 10.10.10.10
    netmask 255.255.255.0
    gateway 10.10.10.1
    dns-nameservers 8.8.8.8
    ```

Kết quả như sau:

```sh
auto eth0
iface eth0 inet static
ipaddress 10.10.10.10
netmask 255.255.255.0
gateway 10.10.10.1
dns-nameservers 8.8.8.8
```

<a name="gachdaudong"></a>

### 5. Gạch đầu dòng

Để sử dụng gạch đầu dòng bạn chỉ cần sử dụng cú pháp sau:

```
- Gạch đầu dòng thứ nhất

  - Thụt với đầu dòng 1

  - Thụt với đầu dòng 1

- Gạch đầu dòng thứ hai

  - Thụt với đầu dòng 2

  - Thụt với đầu dòng 2

```

- Gạch đầu dòng thứ nhất

  - Thụt với đầu dòng 1

  - Thụt với đầu dòng 1

- Gạch đầu dòng thứ hai

  - Thụt với đầu dòng 2

  - Thụt với đầu dòng 2

<a name="taobang"></a>

### 6. Tạo bảng

Bạn có thể sử dụng cú pháp sau để tạo bảng:

```
| Cột 1 Hàng 1 | Cột 2 | Cột 3| Cột 4 |
|--------------|-------|------|-------|
| Hàng 2 | 2 x 1 | 2 x 2 | 2 x 3 | 2 x 4 |
| Hàng 3 | 3 x 1 | 3 x 2 | 3 x 3 | 3 x 4 |
| Hàng 4 | 4 x 1 | 4 x 2 | 4 x 3 | 4 x 4 |
```

Kết quả:

| Cột 1 Hàng 1 | Cột 2 | Cột 3 | Cột 4 |
| ------------ | ----- | ----- | ----- | ----- |
| Hàng 2       | 2 x 1 | 2 x 2 | 2 x 3 | 2 x 4 |
| Hàng 3       | 3 x 1 | 3 x 2 | 3 x 3 | 3 x 4 |
| Hàng 4       | 4 x 1 | 4 x 2 | 4 x 3 | 4 x 4 |

<a name="meo"></a> ###_Mẹo:_

- Sử dụng trang http://markdownlivepreview.com/ paste vào đó đoạn markdown bạn viết và xem trước để chỉnh sửa cho phù hợp.

- Bạn cũng có thể sử dụng những đoạn markdown của người khác đã viết trước để tham khảo.

Như vậy bạn đã có thể trình bày github của mình một cách sáng sủa bằng markdown.

<a name="cacthaotacvoigitvagithub"></a>
