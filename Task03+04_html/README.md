##Task 3+4

---------------------
>Người thực hiện : Ngô Huỳnh Thảo Phương
>
>Tên tài liệu :
>
>https://goo.gl/wHTgSV
>
>https://goo.gl/xLWVHf
>
>Ngày cập nhật: 
>
---------------------

##Mục lục:

[1.HTML là gì? HTML đóng vai trò gì trong website?](#1)

[2.Soạn văn bản HTML.](#2)

[3.Tạo các tài liệu website bằng HTML.](#3)

[4.Một số thẻ khai báo thông tin website.](#4)

[5.Các thẻ định dạng văn bản.](#5)

[6.Thẻ tạo danh sách trong HTML](#6)

[7.Thẻ tạo liên kết.](#7)

[8.Chèn hình ảnh, video, audio và website](#8)

[9.Tạo form nhập liệu.](#9)

##Nội dung

####1.HTML là gì? HTML đóng vai trò gì trong website?<a name="1"></a>

 + HTML (viết tắt bởi HyperText Markup Language) được sử dụng để tạo một trang web, trên một website có thể sẽ chứa nhiều trang và mỗi trang được quy ra là một tài liệu HTML.

![image](http://i.imgur.com/Nr1moln.jpg)

 + HTML có vai trò xây dựng cấu trúc siêu văn bản trên một website, hoặc khai báo các tập tin kỹ thuật số (media) như hình ảnh, video, nhạc và định dạng các siêu văn bản. Trong một website HTML có vai trò hình thành trên website đó.

####2. Soạn văn bản HTML<a name="2"></a>

 + Văn bản HTML bao gồm văn bản và các thẻ html, khi lưu tập tin phải có đuôi là .html

![image](http://i.imgur.com/pXxxWC9.jpg)

 + Cấu trúc 1 đoạn HTML : `thẻ_mở text thẻ_đóng.` 
 
```sh
<p> Văn bản HTML bao gồm văn bản và các thẻ html, khi lưu tập tin phải có đuôi là .html </p>
```

 + Tuy nhiên trong HTML có 1 số thẻ không có thẻ đóng, khi sử dụng bạn nên /> cuối cùng. 

 + Trong mỗi thẻ có những thuộc tính khác nhau, mỗi thuộc tính luôn có một giá trị nào đó. Ta có thể sử dụng nhiều thuộc tính cho 1 thẻ, mỗi thuộc tính được khai báo cách nhau bởi dấu space. 

 + Thuộc tính được khai báo trong thẻ mở như sau: 

```sh
<thẻ_mở tên_thuộc_tính="giá_trị"> Text </thẻ_đóng>
```

**VD** : `<p style="color: blue">Văn bản</p>` --> kết quả : <p style="color: blue">Văn bản</p>

####3. Tạo các tài liệu website bằng HTML<a name="3"></a>

![image](http://i.imgur.com/NlsQSgm.jpg)

Một tài liệu website bắt buộc phải có **thẻ <!DOCTYPE>**. Thẻ này giúp trình duyệt hiểu đây là một tài liệu html, thẻ này không phải là thẻ html. 

Sau đó ta khai báo toàn bộ nội dung websate bằng cặp thẻ <html></html>. Trong cặp thẻ <html></html> có 2 thành phần chính là **head** và **body**. 

Cấu trúc đơn giản bắt buộc của 1 tài liệu website phải có:

```javascript
<!DOCTYPE>
<html>
    <head>
        
    </head>
    <body>
        
    </body>
</html>
```

 + Thẻ `<html> </html>` : phải bao bọc toàn bộ nội dung của website. Tham số hay sử dụng ở đây là lang="mã_ngôn_ngữ"

 + Thẻ `<head> </head>`: khai báo thông tin tài liệu của website như : tên website là gì? mô tả như thế nào? sử dụng bảng mã gì? ...

 + Thẻ `<body></body>`: thẻ chứa toàn bộ đoạn văn bản nằm trong website.

####4.Một số thẻ khai báo thông tin website.<a name="4"></a>

Các thẻ khai báo thông tin cho website bắt buộc phải bỏ trong thẻ:

```sh
<head>

</head>
```

**Thẻ `<title></title>`** : giúp khai báo tên tiêu đề của website

```javascript
<!DOCTYPE>
<html>
	<head>
		<title> Developer Web </title>
	</head>
</html>
```

**Thẻ `<meta thuộc_tính="giá_trị"/>` **: khai báo bảng mã cho webssite. 

Các thuộc tính thường có trong thẻ meta:

 + *charset*: giúp trình duyệt hiểu văn bản website xài bảng mã nào.

```javascript
<!DOCTYPE html>
<html lang="vi">
    <head>
        <meta charset="utf-8" />
    </head>
</html>
```

 + *content* : thuộc tính cung cấp các giá trị liên quan trong các thuộc tính như *name* hay *http-equiv*

```javascript
<!DOCTYPE html>
<html lang="vi">
    <head>
        <meta name="description" content="Học HTML cơ bản" />
    </head>
</html>
```

 + *name* : thuộc tính định nghĩa tên của HTML. Nó có nhiều giá trị đi kèm như :

 		**author**: tên tác giả

```javascript
<!DOCTYPE html>
<html lang="vi">
    <head>
        <meta name="author" content="H C D" />
    </head>
</html>
```

        **language**: dành cho các website không phải tiếng Anh 

```javascrpt
<!DOCTYPE html>
<html lang="vi">
    <head>
        <meta name="language" content="english" />
    </head>
</html>
```

 		**description** : mô tả nội dung của tài liệu website

```javascript
<!DOCTYPE html>
<html lang="vi">
    <head>
        <meta name="description" content="Học HTML cơ bản" />
    </head>
</html>
```
 	
    	**keywords**: từ khóa đại diện cho tài liệu website

```javascript
<!DOCTYPE html>
<html lang="vi">
    <head>
        <meta name="keywords" content="khái niệm,tag,science" />
    </head>
</html>
```

 + *http-equiv* 

        **content-language**: khai báo ngôn ngữ website (dành cho các website không phải tiếng Anh)

```javascript
<!DOCTYPE html>
<html lang="vi">
    <head>
        <meta http-equiv="content-language" content="vi" />
    </head>
</html>
```

        **content-type** : khai báo mã cho website.

```javascript
<!DOCTYPE html>
<html lang="vi">
    <head>
        <meta http-equiv="content-type" content="text/html; charset=utf-8" />
    </head>
</html>
```

####5.Các thẻ định dạng văn bản.<a name="5"></a>

Các thẻ định dạng văn bản bắt buộc phải bỏ trong thẻ:

```sh
<body>

</body>
```

 + Thẻ định dạng tiêu đề: trong đó cỡ chữ sẽ giảm dần từ level 1 -> 6

Cấu trúc: 

```sh
	<h1>Headline level 1</h1>

	<h2>Headline level 2</h2>

	<h3>Headline level 3</h3>

	<h4>Headline level 4</h4>

	<h5>Headline level 5</h5>

	<h6>Headline level 6</h6>
```

Kết quả:

![image](http://i.imgur.com/zgPXJ28.png)

 + Thẻ khai báo đoạn văn bản : `<p> Đoạn_văn_bản </p>`

**VD**: 

```javascript
<!DOCTYPE html>
<html lang="vi">
    <head>
        <meta name="description" content="Học HTML cơ bản" />
        <meta charset="utf-8" />
    </head>
    <body>
        <p> Đoạn văn bản 1 </p>
        <p> Đoạn văn bản 2 </p>
    </body>
</html>
```

Kết quả :

![image](http://i.imgur.com/ZmrtAiF.png)

 + Thẻ in đậm : `</strong> in_đậm </strong>`

**VD**: 

![image](http://i.imgur.com/AFn5znt.png)

```javascript
<!DOCTYPE html>
<html lang="vi">
    <head>
        <meta name="description" content="Học HTML cơ bản" />
        <meta charset="utf-8" />
    </head>
    <body>
        <strong> Ngô Huỳnh Thảo Phương </strong>
    </body>
</html>
```

Kết quả :

 + Thẻ in nghiêng : `<i> in_nghiêng </i>`

**VD**

![image](http://i.imgur.com/TamlbDV.png)

```javascript
<!DOCTYPE html>
<html lang="vi">
    <head>
        <meta name="description" content="Học HTML cơ bản" />
        <meta charset="utf-8" />
    </head>
    <body>
        <i> Huỳnh Chí Duẫn </i>
    </body>
</html>
```

Kết quả:


 + Thẻ gạch chân: `<u> gạch_chân </u>`

**VD**

```javascript
<!DOCTYPE html>
<html lang="vi">
    <head>
        <meta name="description" content="Học HTML cơ bản" />
        <meta charset="utf-8" />
    </head>
    <body>
        <u> Cùng học các thẻ trong HTML </u>
    </body>
</html>
```

Kết quả:

![image](http://i.imgur.com/xAn8ARh.png)

 + Thẻ gạch ngang: `<strike> gạch_ngang </strike>`

**VD**

```javascript
<!DOCTYPE html>
<html lang="vi">
    <head>
        <meta name="description" content="Học HTML cơ bản" />
        <meta charset="utf-8" />
    </head>
    <body>
        <strike> Hôm nay trời không mưa </strike>
    </body>
</html>
```

Kết quả:

![image](http://i.imgur.com/ANLKc0x.png)

 + Thẻ gạch ngang phân đoạn : `<hr>`

**VD**

```javascript
<!DOCTYPE html>
<html lang="vi">
    <head>
        <meta name="description" content="Học HTML cơ bản" />
        <meta charset="utf-8" />
    </head>
    <body>
        <p> Cho em một chỗ bên anh thôi</p>
        <p> Một chỗ khiêm nhu nhất trên đời </p>
        <hr>
        <p> Cho dù anh có đó hay không có </p>
        <p> Em cũng yên lòng nghe bão rơi </p>
    </body>
</html>
```

Kết quả : 

![image](http://i.imgur.com/WnYjxeZ.png)

 + Thẻ trích dẫn: `<quote> trích_dẫn </quote>`

 + Thẻ làm nổi bật: `<cite> text </cite>`

 + Thẻ định dạng sẵn: `<pre> nội_dung </pre>`

**VD** 

```javascript
<!DOCTYPE html>
<html lang="vi">
    <head>
        <meta name="description" content="Học HTML cơ bản" />
        <meta charset="utf-8" />
    </head>
    <body>
        <pre>
            Năm nay đào lại nở
            Không thấy ông đồ xưa
            Những người muôn năm cũ
            Hồn ở đâu bây giờ?
        </pre>
    </body>
</html>
```

Kết quả :

![image](http://i.imgur.com/EGF59Na.png)

 + Thẻ code: `<code> nội_dung </code>`

Thuộc tính *style* được sử dụng trong hầu hết các thẻ. Trong nó có nhiều thuộc tính con như: 
	
	color: màu chữ viết. Vào https://www.w3schools.com/colors/colors_picker.asp để chọn mã màu.

	background-color: màu nền

	font-size: cỡ chữ

	font-family: kiểu chữ.

	text-align: căn lề văn bản. Có 4 chế độ: left, center, right, justify.

**VD**:

```javascript
<!DOCTYPE html>
<html lang="vi">
    <head>
        <meta name="description" content="Học HTML cơ bản" />
        <meta charset="utf-8" />
    </head>
    <body>
        <p style="color: #ff8080; background-color: #3d3d29; font-size: 14; font-family: arial; text-align: left;" > Chiều nay còn mưa sao anh không lại, nhớ mãi trong cơn đau buồn, làm sao có nhau, hằn lên nỗi đau, bước chân em xin về mau. </p>
    </body>
</html>
```

Kết quả: 

![image](http://i.imgur.com/Dr3X0wP.png)

**Chú ý**: thẻ `<span> nội_dung </span>` : dùng để inline 1 đoạn trong văn bản. Cũng có thể kết hợp với thuộc tính style để trang trí và định dạng nội dung.

####6.Thẻ tạo danh sách trong HTML<a name="6"></a>

Trong HTML có hỗ trợ 3 loại danh sách: 

 + Có sắp xếp: Hiển thị list theo thứ tự số, hoặc chữ cái, hoặc chữ số la mã ...

```sh
	<ol thuộc_tính="giá_trị"> 
		<li> Text </li>
		<li> Text </li>
		<li> Text </li>
	</ol>
```

**VD**:

```javascript
<!DOCTYPE>
<html lang="vi">
    <head>
        <title> Developer Web </title>
        <meta charset="utf-8">
    </head>
    <body>
        <h3> Học HTML cơ bản </h3>
        <ol type="1">
            <li> HTLM là gì ? </li>
            <li> Vai trò của HTML </li>
            <li> Tạo tài liệu website bằng HTML </li>
        </ol>
    </body>
</html>
```

 Kết quả: 

 ![image](http://i.imgur.com/n5gAvLA.png)

 + Không sắp xếp: Hiển thị list bởi các dấu chấm đầu dòng.

```sh
 	<ul>
 		<li> Text </li>
		<li> Text </li>
		<li> Text </li>
	</ul>
```

**VD**: 

```javascript
<!DOCTYPE>
<html lang="vi">
    <head>
        <title> Developer Web </title>
        <meta charset="utf-8">
    </head>
    <body>
        <h3> Học HTML cơ bản </h3>
        <ul>
            <li> HTLM là gì ? </li>
            <li> Vai trò của HTML </li>
            <li> Tạo tài liệu website bằng HTML </li>
        </ul>
    </body>
</html>
```

 Kết quả: 

![image](http://i.imgur.com/85VwmbT.png)

 + Có mô tả: Hiển thị danh sách theo cặp tiêu đề- mô tả tiêu đề.

```sh
 	<dl>
 		<dt> Text </dt>
 		<dd> Text </dd>

 		<dt> Text </dt>
 		<dd> Text </dd>

 		<dt> Text </dt>
 		<dd> Text </dd>
 	</dl>
```

**VD**: 

```javascript
<!DOCTYPE>
<html lang="vi">
    <head>
        <title> Developer Web </title>
        <meta charset="utf-8">
    </head>
    <body>
        <dl>
            <dt> HTML là gì? </dt>
            <dd> HTML được sử dụng để tạo một trang web ...</dd>
            <dt> Văn bản HTML là gì? </dt>
            <dd> Văn bản HTML bao gồm văn bản và các thẻ html, khi lưu tập tin phải có đuôi là .html </dd>
        </dl>
    </body>
</html>
```

 Kết quả : 

![image](http://i.imgur.com/ZSY50le.png)

####7.Thẻ tạo liên kết.<a name="7"></a>

Thẻ tạo liên kết trong HTML là `<a thuộc_tính> tên_liên_kết </a>`

Trong thẻ tạo liên kết có nhiều thuộc tính quan trọng như:

 + href : liên kết cần trỏ về.

```javascript
<!DOCTYPE>
<html lang="vi">
    <head>
        <title> Developer Web </title>
        <meta charset="utf-8">
    </head>
    <body>
        <a href="https://goo.gl/xLWVHf"> Học HTML cơ bản </a>
    </body>
</html>
```
 Kết quả:

![image](http://i.imgur.com/Pfzs2F4.png)

 + title : thiết lập tiêu đề.

```javascript
<!DOCTYPE>
<html lang="vi">
    <head>
        <title> Developer Web </title>
        <meta charset="utf-8">
    </head>
    <body>
        <a href="https://goo.gl/xLWVHf" title="tài liệu HTML"> Học HTML cơ bản </a>
    </body>
</html>
```
 Kết quả: 

 ![image](http://i.imgur.com/uBPj5ow.png)

 + target : thiết lập cửa sổ mở tập tin từ liên kết. Trong target có 2 giá trị:

        _blank: thiết lập liên kết mở ra cửa số mới.

        _self: mở tập tin trên cửa sổ hiện tại
 
Ngoài ra, ta còn có một loại liên kết khác là liên kết neo. Liên kết giúp nhảy đến một đoạn hay một khu vực nào đó trong cùng một văn bản.

```javascript
<a href="#nội_dung">tên_liên_kết</a> : nơi cần tạo liên kết

<tên_thẻ id="#nội_dung"> Text </tên_thẻ>
```

####8.Chèn hình ảnh, video, audio và website<a name="8"></a>

 + Thẻ chèn hình ảnh : `<img />`
 
 Trong thẻ có nhiều thuộc tính quan trọng như :

    src : source, đường dẫn muốn chèn vào; phải là một liên kết trực tiếp.

    alt : đoạn mô tả hình ảnh không hiện ra.

    title : tiêu đề cho đường dẫn.

    width : khai báo kích thước chiều rộng của ảnh.

    height : khai báo kích thước chiều rộng của ảnh.

**VD** 

```javascript
<!DOCTYPE html>
<html>
    <head>
        <title> Developer Web </title>
        <meta charset="utf-8">
    </head>
    <body>
        <p> Nhìn là 10 nghìn </p>
        <img src="http://i.imgur.com/GlYWf1b.jpg" alt="ba con heo là beo con ha" title="xàm team" width="300px" height="auto" />
    </body>
</html>
```
 
 ![image](http://i.imgur.com/KtQDkfp.png)
 
 + Thẻ chèn video : ` <video thuộc_tính> </video> `
 
 Trong thẻ có nhiều thuộc tính như:

    width: chiều rộng của màn hình video

    height: chiều dài của màn hình video

    type: khai báo định dạng video.

 Trong thẻ `<video></video>` có thẻ khác nữa là thẻ : 

    `<source src="đường_dẫn />"`

 + Thẻ chèn audio: `<audio controls> </audio>`
 
 Trong thẻ `<audio></audio>` đi kèm với thẻ: `<source src="đường_dẫn" />`

 + Thẻ chèn website : `<iframe src="đường_dẫn" thuộc_tính></iframe>`
 
 Trong thẻ có nhiều thuộc tính như:

    width : chiều rộng website

    height : chiều dài website

    scrolling : thiết lập thanh trượt.

Ngoài ra, iframe còn được dùng để tạo liên kết sau đó tải bằng iframe.

Ví dụ :

####9.Tạo form nhập liệu.<a name="8"></a>  

Form nhập liệu : nghĩa là form có thể điền thông tin vào và gửi đi.

Ta dùng thẻ : 

```sh 
<form thuộc_tính> 

    <input thuộc_tính />

</form>
```

Trong thẻ `<form>` có những thuộc tính bắt buộc :
    
    action : khai báo đường dẫn khi người dùng gửi form đi.

    method : khai báo dữ liệu gửi đi theo phương thức nào. Có 2 giá trị : post, get.

    name : tên của form.

Các thuộc tính trong thẻ `<input />` :
    
    type : loại trường dữ liệu cần nhập vào. Trong type có nhiều giá trị khác nhau như : text, passwork, submit, ...

    name : tên trường dữ liệu.

    date : ngày tháng.

    *Tham khảo thêm tại* : https://goo.gl/B5RWRw











 





