##Task 6
-----------------

>Người thực hiện: Ngô Huỳnh Thảo Phương
>
>Tên tài liệu:
>
>https://goo.gl/x7Z4ll
>
>https://goo.gl/pp3Fwg
>
>https://goo.gl/1mgkiz
>
>Ngày cập nhật: 25/04/2017
---------------------------

##Mục lục:

[1. CSS là gì? Vai trò của CSS trên website? Cách nhúng CSS vào website](#1)

[2. Cú pháp và bộ chọn của CSS.](#2)

[3. CSS Color. CSS Height/Width.](#3)

[4. CSS Backgrounds](#4)

[5. CSS Borders](#5)

[6. CSS Margins](#6)
 
[7. CSS Padding](#7)

[8. CSS Box Model](#8)

[9. CSS Outline](#9)

[10. CSS Text](#10)

[11. CSS Fonts](#11)

[12. CSS Links](#12)

[13. CSS Lists](#13)

[14. CSS Tables](#14)

##Nội dung:

####1. CSS là gì? Vai trò của CSS trên website?<a name="1"></a>

######CSS là gì?

CSS (Cascading Style Sheets) là ngôn ngữ miêu tả định dạng của tài liệu HTML. CSS miêu tả các thẻ HTML được hiển thị như thế nào.

######Vai trò của CSS trên website?

Trên website nó đóng vai trò làm đẹp, định dạng website như chia cột, thêm màu sắc, biến đổi các khối,..

######Cách nhúng CSS vào website :

 + Cách 1 : Inline Style sheet

 Là chèn thẳng CSS vào tài liệu HTML.

 Chèn bằng cặp thẻ ` <style> </style> `. Cặp thẻ này thường được đặt trong cặp thẻ `<head> </head>`.

 Trong thẻ `<style>` có tham số tên `type` với tham số `"text/css"`

 **Ví dụ : **

 ```sh
 	<!DOCTYPE html>
 	<html lang="vi">
 		<head>
 			<meta charset="utf-8" />
 			<title> Nhúng CSS kiểu Inline </title>
 			<style type="text/css">
 				p {
 					color: white;
 				}
 			</style>
 		</head>
 		<body>
 			<p> Đây là đoạn văn bản </p>
 		</body>
 	</html>
 ```

 + Cách 2 : Extermal Style sheet

 Là tạo một file CSS riêng sau đó dùng phần tử `<link>` để nhúng CSS file vào trong tài liệu HTML. 

 Tương tự Inline, thẻ `<link>` được đặt trong cặp thẻ `<head> <//head>`. Trong thẻ `<link>` có các tham số: rel với giá trị `"stylesheet"`, href với giá trị là đường dẫn chứa file CSS, type với giá trị là text/css.

 **Ví dụ: **

 ```sh
 	<!DOCTYPE html>
 	<html lang="vi">
 		<head>
 			<meta charset="utf-8" />
 			<title> Nhúng CSS kiểu Inline </title>
 			<link rel="stylesheet" href="style.css" />
 		</head>
 		<body>
 			<p> Đây là đoạn văn bản </p>
 		</body>
 	</html>
 ```

 + Cách 3: Inline style

 Sử dụng bằng cách thêm thuộc tính `style` vào phần tử có liên quan. Thuộc tính `style` có thể chứ bất kì thuộc tính css nào.

 **Ví dụ: **

 ```sh
 	 <h1 style="color:blue;margin-left:30px;">This is a heading</h1>
 ```

Tuy nhiên cách 3 ít được sử đụng vì độ thiếu hiệu quả của nó.

####2. Cú pháp và bộ chọn của CSS<a name="2"></a>

######a. Cú pháp của CSS

```sh
	Vùng chọn {
		thuộc-tính: giá trị; 
		thuộc-tính: giá trị;
		...
		("thuộc-tính: giá trị;": gọi là 1 khai báo )
	}
```

 + Vùng chọn chỉ các thẻ HTML bạn muốn định dạng.

 + Khối khai báo chứa một hoặc nhiều khai báo cách nhau bởi dấu chấm phẩy.

 + Mỗi khai báo bao gồm một tên thuộc tính CSS và một giá trị, được phân cách bởi dấu hai chấm.

 + Một khai báo CSS luôn luôn kết thúc bởi một dấu chấm phẩy, và các khối khai báo được bao quanh bởi các dấu ngoặc nhọn.

**Ví dụ :** 

```sh
	p {
		color : blue;
		text-align: center;
	}
```

######b.Bộ chọn của CSS:

Bộ chọn CSS được sử dụng để "tìm" (hoặc chọn) phần tử HTML dựa trên tên phần tử, id, lớp, thuộc tính của chúng và hơn thế nữa.

 + Bộ chọn nguyên tố: 

 Bộ chọn nguyên tố chọn các phần tử dựa trên tên phần tử.

 **Ví dụ**: 

Bạn có thể chọn tất cả các phần tử `<p>` trên tài liệu HTML (trong trường hợp này, tất cả các phần tử `<p>` sẽ được căn giữa, có màu đỏ):

```sh 
	p {
		color: red;
		text-align: center;
	}
```

+ Bộ chọn id: 

Bộ chọn id sử dụng thuộc tính id của một phần tử HTML để chọn một phần tử cụ thể.

Id của một phần tử phải là duy nhất trong một trang, vì vậy bộ chọn id được sử dụng để chọn một phần tử duy nhất.

Để chọn một phần tử có id cụ thể, sử dụng kí tự (#), tiếp theo là id của phần tử.

**Ví dụ :**

Định dạng cho phần tử HTML với `id="hoccss"` :

```sh
	#hoccss {
		color: blue;
		text-align: right;
	}
```

Ghi chú: Tên của id không được bắt đầu bằng một chữ số.

+ Bộ chọn class:

Bộ chọn class chọn các phần tử có thuộc tính lớp cụ thể.

Để chọn các phần tử với một lớp cụ thể, sử dụng ký tự (.), tiếp theo là tên của lớp.

**Ví dụ: **

Tất cả các phần tử HTML với `class = "test" sẽ được định dạng màu xám và căn phải :

```sh
	.test {
		text-align: right;
		color: grey;
	}
```

Ngoài ra, bạn cũng có thể chỉ định các phần tử HTML cụ thẻ sẽ bị ảnh hưởng bởi lớp đã chọn, bằng các thêm tên các phần tử HTML trước dấu (.). 

**Ví dụ: **

Chỉ các phần tử `<p>` với `class = "test" sẽ được căn giữa và có màu đỏ.

```sh
	p.test {
		text-align : center;
		color: red;
	}
```

+ Bộ chọn nhóm:  

Để giảm thiểu mã, người ta sử dụng nhóm các bộ chọn. Các bộ chọ được nhóm lại tách riêng nhau bởi dấu phẩy.

**Ví dụ : **

```sh
	h1, h2, p {
		color: green;
		text-align: right;
	}
```

Ngoài ra, cách tạo comment trong CSS: 

```sh
	/* text */
```

####3. CSS Color. CSS Height/Width.<a name="3"></a>

 + CSS Color: Màu sắc trong CSS thường được chỉ định bởi:

    Tên màu hợp lệ như :  "màu đỏ"

    Một giá trị RGB như: "rgb (255, 0, 0)"

    Giá trị HEX như : "#ff0000"

 + CSS Height/Width : được dùng để thiết lập chiều cao và chiều rộng của phần tử.

 	Chiều cao và chiều rộng của phần tử có thể đặt auto (mặc định) hoặc sử dụng các giá trị chiều dài : px, pt, cm, etc .. hoặc cũng có thể sử dụng %.

 Max-width : được sử dụng để đặt chiều rộng tối đa của một phần tử. Thuộc tính này nhận giá trị tương tự với thuộc tính width.

 Sự khác nhau khi sử dụng giữa max-width và width :

 		Khi sử dụng width, nếu chiều rộng của cửa sổ trình duyệt nhỏ hơn chiều rộng của phần tử, trình duyệt sẽ thêm thanh cuộn ngang vào trang.

 		Khi sử dụng với max-width : trong trường hợp này sẽ cải thiện việc xử lí các trình duyệt của các cửa sổ nhỏ.

####4.CSS Backgrounds<a name="4"></a>

Thuộc tính nền của CSS Background gồm :

		background-color

    	background-image

    	background-repeat

    	background-attachment

    	background-position

 + Background-color: xác định màu nền của một phần tử.

 		```sh
 			vùng chọn {
 				background-color: #083096
 			}
 		```

 + Background-image: thiết lập hình nền cho một phần tử. 
 		
 		```sh
 			vùng chọn {
 				background-image: url("link_ảnh");
 			}
 		```

 + Background-repeat: thiết lập cách một hình nền sẽ được lặp lại. Có 3 giá trị lựa chọn:

 	repeat-x: lặp lại theo chiều ngang.

 	repeat-y: lặp lại theo chiều dọc.

 	no-repeat: không lặp lại.

 		```sh
 			vùng chọn {
 				background-style: solid;
 				bacckground-repeat : repeat-x;
 			}
 		```

 + Background-attachment: thiết lập xem ảnh nền đã được cố định hay cuộn với phần còn lại của trang. đi kèm với giá trị `fixed`

 		```sh
 			vùng chọn {
 				background-attachment: fixed;
 			}
 		```
 
 + Background-position: đặt vị trí bắt đầu của một hình nền.

 		```sh
 			vùng chọn {
 				background-position: right top;
 			}
 		```

Ngoài ra, để rút ngắn mã, ta có thể chỉ định tất cả thuộc tính nền trong một thuộc tính duy nhất.

	```sh
		vùng chọn {
			background: color image repeat position;
		}
	```

####5. CSS Borders<a name="5"></a>

Thuộc tính CSS Border cho phép bạn chỉ định kiểu, chiều rộng và màu sắc của đường viền border.

 + Border Style : chỉ định loại đường biên hiển thị. Các giá trị có trong border style :

 		dotted : đường kẻ chấm. 

 		dashed : đường viền đứt.

 		solid : đường viền đậm.

 		double : đường viền đôi.

 		groove : đường viền rãnh 3D, phụ thuộc vào màu của đường viền.

 		ridge : đường viền biên 3D, phụ thuộc vào màu của đường viền.

 		inset : đường biên bên trong 3D, phụ thuộc vào màu của đường viền.

 		outset : đường biên bên ngoài 3D, phụ thuộc vào màu của đường viền.

 		none : không đường viền.

 		hidden : đường viền ẩn.

 		mix: chọn nhiều kiểu đường viền, tối đa 4.

 Thuộc tính border-style có thể có từ 1 đến 4 giá trị (tương ứng đường viền trên cùng, phải, bên dưới và trái ).

** Ví dụ : **

```sh
	p.dotted {border-style: dotted;}
	p.dashed {border-style: dashed;}
	p.solid {border-style: solid;}
	p.double {border-style: double;}
	p.groove {border-style: groove;}
	p.ridge {border-style: ridge;}
	p.inset {border-style: inset;}
	p.outset {border-style: outset;}
	p.none {border-style: none;}
	p.hidden {border-style: hidden;}
	p.mix {border-style: dotted dashed solid double;}
```

 + Border Width : chỉ chiều rộng của 4 đường viền. Chiều rộng có thể được xác định bởi :

 		kích thước đo cụ thể : in, px, pt, cm, em, etc

 		giá trị xác định : thin, medium, thick.

 Thuộc tính border-width có thể có từ 1 đến 4 giá trị.

 **Ví dụ : **

 ```sh 
 	p.one {
    	border-style: solid;
    	border-width: 5px;
	}
 ```
 
 + Border-color : chỉ định màu cuả 4 đường viền. Màu được xác định bởi :

 	tên màu.

 	HEX: giá trị hex ( ví dụ: #ffffff ).

 	RGB: giá trị RGB ( ví dụ: rgb(255,165,0) ).

 	transparent ( trong suốt ).

 ```sh 
 	vùng chọn {
 		border-style: double;
 		border-color: blue;
 	}
 ```

Bạn có thể chỉ định tất cả các thuộc tính cho một bên của border bằng các thuộc tính : border-top, border-right, border-bottom, border-left.

** Ví dụ: **

```sh 
	p {
    	border-bottom: 6px solid red;
    	background-color: lightgrey;
	}
```

Ngoài ra, để rút gọn mã, người ta có thể chỉ đinh các thuộc tính nền trong một thuộc tính duy nhất.

```sh 
	vùng chọn {
		border: color style width ;
	}
```

####6. CSS Margins (Căn lề) <a name="6"></a>

Các thuộc tính nền của CSS Margins :

		margin-top

		margin-right

		margin-bottom

		margin-left

Tất cả các thuộc tính lề có các giá trị sau :

		auto : trình duyệt tính lề tự động.

		chiều dài : chỉ định lề bằng px, pt, cm, etc

		% : chỉ định lề bằng % độ rộng phần tử chứa.

		inherit : lề được xác đinh dựa trên phần tử cha.

	Các giá trị âm vẫn được phép sử dụng.

** Ví dụ : **

```sh
	p {
		magin-top: 100px;
		magin-bottom : 100px;
		magin-right: 150px;
		magin-left : 50px;
	}
```

Ngoài ra, ta có thể rút gọn mã bằng việc thay thế các thuộc tính nền bằng một thuộc tính duy nhất. 

```sh
	vùng chọn {
		magin: top right bottom left;	
	}
```

Cách hoạt động của các giá trị trong margin :

 + Nếu thuộc tính margin có 4 giá trị :
 	
 	`margin: 25px 50px 75px 100px ;`

 		lề trên là : 25px

 		lề phải là : 50px

 		lề dưới là : 75px

 		lề trái là : 100px

 + Nếu thuộc tính margin có 3 giá trị :

 	`margin: 25px 50px 75px ;`

 		lề trên là : 25px

 		lề phải là : 50px

 		lề dưới là : 75px

 + Nếu thuộc tính margin có 2 giá trị :

 	`margin: 25px 50px ;`

 		lề trên và lề dưới là : 25px

 		lề phải và lề trái là : 50px

 + Nếu thuộc tính margin có 1 giá trị :

 	`margin 25px ;`

 		tất cả 4 lề là 25px

####7. CSS Padding (Vùng đệm) <a name="7"></a>

Các thuộc tính đệm tạo khoảng trống xung quanh nội dung. Các thuộc tính nền của CSS Padding : 

		padding-top

		padding-right

		padding-bottom

		padding-left

Tất cả các thuộc tính đệm đều có các giá trị sau :

		chiều dài: chỉ định đệm bằng px, pt, cm, etc.

		% : chỉ định bằng % độ rộng phần tử chứa

		inherit : kế thừa từ phần tử cha.

** Ví dụ : **

```sh
	p {
		padding-top: 100px;
		padding-bottom : 100px;
		padding-right: 150px;
		padding-left : 50px;
	}
```

Ngoài ra, ta có thể rút gọn mã bằng việc thay thế các thuộc tính nền bằng một thuộc tính duy nhất. 

```sh
	vùng chọn {
		padding : top right bottom left;	
	}
```

Cách hoạt động của các giá trị trong Padding tương tự như trong Margin.

####8. CSS Box Model <a name="8"></a>

Tất cả các phần tử HTML được xem như các hộp. Trong CSS, thuật ngữ "Box Model" được sử dụng để nói về cách bố trí và thiết kế các phần tử HTML.

Box Model về cơ bản là một hộp bao quanh mọi phần tử HTML. Nó bao gồm : lề, biên, đệm và nội dung.

Giải thích về các phần trong Box Model :

		Content : nội dung của hộp, nơi văn bản và hình ảnh xuất hiện.

		Padding : xóa một khu vực xung quanh nội dung. Phần đệm là trong suốt.

		Border : đường viền quanh khoảng đệm và nội dung.

		Margin : xóa một khu vực bên ngoài biên. Phần lề là trong suốt.

Box Model cho phép chúng ta thêm một đường viền xung quanh các phần, để xác định không gian của các phần tử.

Để đặt chiều rộng và chiều cao cho phần tử một cách chính xác trong tất cả các trình duyệt, bạn phải biết cách làm việc của mô hình.

**Ghi chú :** Khi đặt chiều rộng và chiều cao của một phần tử trong CSS, chỉ cần đặt chiều rộng và cao của nội dung. Để tính toán kích thước đầy đủ của một phần tử. bạn phải thêm padding, borders and margins.

 + Cách tính tổng chiều rộng của một phần tử:

 		Tổng chiều rộng = width + left-padding + right-padding + left border + right-border + left-margin + right-margin.

 + Cách tính tổng chiều cao của một phần tử : 

 		Tổng chiều cao = height + top-padding + bottom-padding + top-border + bottom-border + top-margin + bottom-margin. 

####9. CSS Outline <a name="9"></a>

Outline là một đường kẻ được vẽ xung quanh các phần tử ( ngoài border ) để làm phần tử nổi bật. Thuộc tính Outline chỉ rõ kiểu, màu sắc và chiều rộng.

Tuy nhiên, outline khác với border, out không là một phần kích thước của phần tử nên tổng chiều rộng và chiều cao của phần tử không bị ảnh hưởng bởi chiều rộng của outline.

 + Outline Style : chỉ định kiểu cho đường outline.

 Outline-style nhận các giá trị : 

 		dotte : đường outline chấm.

 		ddashed : đường outline đứt.

 		solid : đường outline đậm.

 		double : đường outline đôi.

 		groove : đường outline rãnh 3D, phụ thuộc vào màu của đường outline.

 		ridge : đường outline biên 3D, phụ thuộc vào màu của đường outline.

 		inset : đường biên bên trong 3D, phụ thuộc vào màu của đường outline.

 		outset : đường biên bên ngoài 3D, phụ thuộc vào màu của đường outline.

 		none : không có đường outline.

 		hidden : đường outline ẩn.

** Ví dụ : **

 	```sh
 		vùng chọn {
 			border : 2px solid grey;
 			outline-style : dotted ;
 		}
 	```

 + Outline Color : chỉ định màu cho đường outline.

 Màu sắc có thể được thiết lập bằng : 

 		Tên : chỉ định tên màu. Ví dụ : red, blue, grey, etc.

 		RGB : chỉ định một giá trị rgb như rgb(255,165,50).

 		Hex : chỉ đinh một giá trị Hex như #ffff00

 		Invert : đảo ngược màu ( đảm bảo đường outline có thể nhìn thấy, bất kể màu nền).

** Ví dụ : **

	```sh
		vùng chọn {
			border : 5px dotted white;
			outline-style : outset ; 
			outline-color : green ;
		}
	```

 + Outline Width : chỉ định độ rộng cho đường outline.

 Chiều rộng của đường outline có thể thiết lập bằng : một kích thước cụ thể ( theo px, pt, cm, em, etc.) hoặc bằng 1 trong 3 giá trị được xác định trước : thin, medium, thick.

** Ví dụ : **

	```sh 
		vùng chọn {
			border : 3px outset pink ;
			outline-style : ridge ;
			outline-width : medium ;
		}
	```

Ngoài ra, ta có thể rút gọn mã bằng việc thay thế các thuộc tính nền bằng một thuộc tính duy nhất.

	```sh 
		vùng chọn {
			outline : width style color ; 
		}
	```

####10. CSS Text <a name="10"></a>

######Text Color : chỉ định màu cho đoạn văn bản.

	Các giá trị màu :

		tên : chỉ định tên màu. Ví dụ : red, blue, grey, etc.

 		RGB : chỉ định một giá trị rgb như rgb(255,165,50).

 		Hex : chỉ đinh một giá trị Hex như #ffff00

 Ngoài ra, xem các giá trị màu CSS có thể có tại https://goo.gl/d70Pam.

** Ví dụ : **

	```sh
		vùng chọn {
			color : grey ;
		}
	```

######Text Alignment: 

Thuộc tính text-align được sử dụng để thiết lập sự sắp xếp ngang của một văn bản.

Khi thuộc tính text-align được đặt thành "justify", mỗi dòng sẽ được kéo dài để mỗi dòng có chiều rộng bằng nhau, và lề trái,phải thẳng hàng. (thường được sử dụng trong các tạp chí, báo).

** Ví dụ : **

	```sh
		vùng chọn {
			text-align : right ;
		}
	```

######Text Decoration 

Thuộc tính dùng để thiết lập hoặc loại bỏ trang trí ra khỏi văn bản.

Thuộc tính text-decoration nhận các giá trị : 

		none : không trang trí.

		overline : gạch trên văn bản. 

		line-through : gạch ngang văn bản.

		underline : gạch dưới văn bản.

** Ví dụ : **

	```sh
		vùng chọn {
			text-decoration : none;
		}
	```

######Text transformation 

Thuộc tính chuyển đổi văn bản để định dạng kiểu chữ hoa hay chữ thường trong văn bản.

Thuộc tính text-transform nhận các giá trị :

		uppercase : tất cả kí tự đều được in hoa.

		lowercase : tất cả kí tự đều được in thường.

		capitalize : in hoa các kí tự đầu tiên.

** Ví dụ : **

	```sh 
		vùng chọn {
			text-transform : capitalize ;
		}
	```

######Text Indentation

Thuộc tính text-indent chỉ định vị trí dòng đầu tiên của văn bản. 

** Ví dụ : **

	```sh
		vùng chọn {
			text-indent : 30px ;
		}
	```

######Letter Spacing

Thuộc tính letter-spacing xác định khoảng cách giữa các kí tụ trong văn bản.

** Ví dụ : **

	```sh
		vùng chọn {
			letter-spacing : 3px;
		}
	```

######Line Height

Thuộc tính line-height xác định khoảng cách giữa các dòng trong văn bản.

** Ví dụ : **

	```sh
		vùng chọn {
			line-height : 0.8 ;
		}
	```

######Text Direction 

Thuộc tính direction sử dụng để thay đổi hướng văn bản của một phần tử. Thuộc tính này nhận giá trị rtl.

** Ví dụ : **

	```sh
		vùng chọn {
			direction : rtl ;
		}
	```

######Word Spacing

Thuộc tính word-spacing dùng để xác định không gian giữa các từ trong văn bản.

** Ví dụ : **

	```sh
		vùng chọn {
			word-spacing : -5px ;
		}
	```

######Text Shadow

Thuộc tính text-shadow dùng để thêm bóng vào văn bản.

Thuộc tính gồm có 3 giá trị đó là : bóng ngang ( horizontal ), bóng đứng ( vertical ) và màu sắc của bóng. 

**Ví dụ : **

	```sh
		vùng chọn {
			text-shadow : 3px 2px grey ;
		}
	```

####11. CSS Fonts <a name="11"></a>

Trong CSS, có 2 loại tên phông chữ : 

	Generic family : một nhóm font families có nét tương tự ( như "Serif" hay "Monospace").

	Font family : một gia đình font chữ cụ thể ( như "Times New Roman" hoặc "Arial").

|Generic family | Font family | Description |
|---------------|-------------|-------------|
|Serif | Times New Roman | có các đường nhỏ ở đầu trên một số kí tự |
|	   | Georgia 		 |
|Sans-serif | Arial   	 | không có dòng ở cuối kí tự |
|			| Verdana 	 |
|Monospace | Courier New | Tất cả các kí tự có cùng chiều rộng. |
|		   | Lucida Console |

######Font Family :

Ta nên bắt đầu với phông chữ mình muốn và kết thúc bằng một generic family, để cho trình duyệt chọn một phông chữ tương tự trong generic family khi không có phông chữ phù hợp. 

Lưu ý : Nếu tên phông chữ có nhiều hơn 1 từ, ta phải bỏ trong dấu ngoặc kép `" "`. Và các phông chữ dự trữ cách nhau bởi dấu phẩy `,`.

** Ví dụ : **

```sh 
	p {
		font-family : "Times New Roman", Times, serif ;
	}
```

Đây là các phông chữ thường được sử dụng : https://goo.gl/LlY1qF

######Font Style :

Thuộc tính có 3 giá trị :

		Normal : văn bản hiển thị bình thường.

		Italic : văn bản thể hiện bằng chữ in nghiêng.

		Oblique : chữ xiên gần giống với in nghiêng, ít được sử dụng.

** Ví dụ : **

```sh
	p {
		font-style: italic ;
	}
```

######Font Size : 

Thuộc tính font-size thiết lập kích thước của văn bản.

Giá trị của thuộc tính có thể là một giá trị tương đối hoặc tuyệt đối. 

 + Kích thước tuyệt đối :

 	Đặt văn bản cho một kích thước được chỉ định. 

 	Không cho phép người dùng thay đổi kích thước văn bản trong tất cả các trình duyệt. 

 	Kích thước tuyệt đối hữu ích khi kích thước vật lý của đầu ra được biết.

 + Kích thước tương đối :

 	Thiết lập kích thước tương đối cho các phần tử xung quanh. 

 	Cho phéo người dùng thay đổi kích thước văn bản trong trình duyệt.

Ta có thể thiết lập giá trị kích thước của văn bản bằng pixels hoặc em. 

Để cho phép người dùng thay đổi kích thước văn bản (trong trình duyệt đơn ) nhiều developers đã sử dụng em thay vì pixels.

		1em = 16px

		em = pixels / 16 

Ngoài ra, ta có thể kết hợp giá trị % và em. Giải pháp hoạt động trong tất cả các trình duyệt là đặt cỡ phông mặc định ở % cho phần tử <body>.

** Ví dụ : **

```sh 
	body {
		font-size: 100% ;
	}

	h1 {
		font-size : 2.5em ;
	}
```

######Font Weight : 

Thuộc tính font-weight thiết lập trọng lượng của phông chữ. 

Thuộc tính này nhận các giá trị như : normal, bold, lighter, lightest, ... Hay cũng có thể nhận các giá trị đo như px, pt, em, cm, etc.

** Ví dụ : **

```sh 
	p {
		font-weight : bold ;
	}
```

######Font Variant : 

Thuộc tính font-variant : cho biết văn bản hiển thị trong một phông chữ nhỏ hay không.

Trong một phông chữ nhỏ, tất cả các chữ thường được chuyển thành chữ hoa. Tuy nhiên, các chữ in hoa được chuyển đổi xuất hiện ở cỡ chữ nhỏ hơn so với chữ in hoa ban đầu trong văn bản.

Thuộc tính này nhận giá trị : normal, small-caps .

** Ví dụ : **

```sh
	p {
		font-variant : small-caps ;
	}
```

**Ghi chú **: Để rút gọn mã, ta có thể thay thế các thuộc tính nền bằng một thuộc tính duy nhất.

```sh 
	vùng chọn {
		font : giá-trị giá-trị ... ;
	}
```

####12. CSS Links <a name="12"></a>

######Styling Links :

Links có thể được tạo với bất kì thuộc tính nào trong CSS. (như color, font-family, background, etc.)

Có 4 liên kết là : 

		a:link - một liên kết bình thường, chưa được kiểm tra. 

		a:visited - một liên kết mà người dùng đã truy cập. 

		a:hover - một liên kết khi người sử dụng chuột lên nó. 

		a:active - một liên kết khi được nhấp vào.

Khi cài đặt trạng thái của link , có một số qui tắc sau :

		a:hover phải đi sau a:link và a:visited.

		a:active phải đi sau a:hover.

**Ví dụ : **

```sh
	vùng chọn {
		a:visited
	}
```

######Text Decoration : 

Thuộc tính text-decoration chủ yếu sử dụng để bỏ đường gạch dưới của links.

**Ví dụ : ** 

```sh
a:link {
	text-decoration : none ;
}
```

######Advanced- Link Buttons :

Ta có thể kết hợp một số thuộc tính trong CSS để biểu diễn cho nút Link.

**Ví dụ :**

```sh
	a:link, a:visited {
    	background-color: #f44336;
    	color: white;
    	padding: 14px 25px;
    	text-align: center;
    	text-decoration: none;
    	display: inline-block;
	}

	a:hover, a:active {
    	background-color: red;
	}
```

####13. CSS Lists <a name="13"></a>

Thuộc tính list trong CSS cho phép bạn :

		Đặt các dấu hiệu mục danh sách khác nahu cho các danh sách có thứ tự.

		Đặt các nhãn mục danh sách khác nhau cho các danh sách không có thứ tự.

		Đặt một hình ảnh làm điểm đánh dấu mục danh sách.

		Thêm màu nền vào danh sách và các mục trong danh sách.

######Different List Item Markers : 

Thuộc tính list-style-type chỉ rõ điểm dánh dấu mục danh sách.
Ta có một số giá trị sẵn có như : circle, square, upper-roman, lower-alpha.

**Ví dụ : **

```sh
	ul.a {
    	list-style-type: circle;
	}

	ul.b {
    	list-style-type: square;
	}
```

Lưu ý : một số giá trị phù hợp cho danh sách sắp xếp, và một sô phù hợp cho danh sách không sắp xếp. 

######An Image as The List Item Marker

Thuộc tính list-style-image chỉ định một hình ảnh như một điểm đánh dấu của danh sách.

**Ví dụ : **

```sh 
	ul {
    	list-style-image: url('sqpurple.gif');
	}
```

######Position The List Item Markers

Thuộc tính list-style-position xác định xem các mục danh sách xuất hiện bên trong hay bên ngoài luồng nội dung. 

**Ví dụ : **

```sh
	ul {
    	list-style-position: inside;
	}
```

######Xóa cài đặt mặc định

Thuộc tính list-style-type được sử dụng để loại bỏ các  markers/bullets. 

Lưu ý : danh sách cũng có margin và padding mặc định, để loại bỏ giá trị này, ta thêm margin : 0; và padding:0 .

**Ví dụ : **

```sh
	ul {
    	list-style-type: none;
    	margin: 0;
    	padding: 0;
	}
```

Ngoài ra, để rút gọn mã, người ta thay các thuộc tính nền bằng thuộc tính duy nhất list-style. Thứ tự của các thuộc tính là : 

		list-style-type.

		list-style-position.

		list-style-image.

** Ví dụ : **

```sh 
	ul {
    	list-style: square inside url("sqpurple.gif");
	}
```

######Styling List With Colors

Thêm màu sắc cho List bằng các thuộc tính có trong CSS.

** Ví dụ : **

```sh
	ol {
    	background: #ff9999;
    	padding: 20px;
	}

	ul {
   	 background: #3399ff;
    	padding: 20px;
	}

	ol li {
   	background: #ffe5e5;
    	padding: 5px;
    	margin-left: 35px;
	}

	ul li {
    	background: #cce5ff;
    	margin: 5px;
	}
```

####14. CSS Tables <a name="14"></a>

Thuộc tính border dùng để định dạng bảng trong CSS.

Thuộc tính border-collapse xác định các đường viền của bảng có nên thu gọn thành một đường viền đơn không.

** Ví dụ :**

```sh 
table {
    border-collapse: collapse;
}

table, th, td {
    border: 1px solid black;
}
```

Nếu bạn chỉ muốn mỗi đường viền bao quanh bảng, sử dụng thuộc tính border cho thẻ `<table>`.

** Ví dụ : **

```sh
table {
    border: 1px solid black;
}
```

######Table Width and Height

Chiều dài và chiều rộng của bảng được xác đinh bởi các thuộc tính width và height.

**Ví dụ :**

```sh
table {
    width: 100%;
}

th {
    height: 50px;
}
```

######Horizontal Alignment

Thuộc tính text-align thiết lập sự sắp xếp theo chiều ngang (left, right and center) của nội dung trong các thẻ : `<th>` hay `<td>`.

Theo mặc định, nội dung trong các thẻ `<th>` được căn giữa và nội dung trong các thẻ `<td>` được căn lề trái.

**Ví dụ : **

```sh
th {
    text-align: left;
}
```

######Vertical Alignment

Thuộc tính vertical-align thiết lập sự sắp xếp theo chiều dọc (top, bottom hay middle) nội dung trong các thẻ `<th>` hay `<td>`.

Theo mặc định, nội dung trong bảng căn chỉnh theo chiều dọc là giữa cho cả thẻ `<th>` và thẻ `<td>`.

**Ví dụ : **

```sh
td {
    height: 50px;
    vertical-align: bottom;
}
```

######Table Padding

Sử dụng thuộc tính padding để kiểm soát không gian giữa border và nội dung trong bảng. 

**Ví dụ : **

```sh
th, td {
    padding: 15px;
    text-align: left;
}
```

######Horizontal Dividers

Để thiết lập đường chia ngang của bảng, ta sử dụng thuộc tính border-bottom.

** Ví dụ : **

```sh
th, td {
    border-bottom: 1px solid #ddd;
}
```

######Hoverable Table

Tạo hiệu ứng màu của hàng khi di chuyển chuột trên bảng ta sử dụng `tr:hover`.

** Ví dụ : **

```sh 
	tr:hover {background-color: #f5f5f5}
```

######Striped Tables

Tạo ra bảng sọc ngựa vằn ( 2 màu xen kẻ giữa các hàng của bảng). Ta sử dụng bộ chọn `tr:nth-child(even/odd)`.

**Ví dụ : **

```sh
	tr:nth-child(even){background-color: #30ff08}
```

Ngoài ra, sử dụng thuộc tính background-color để thiết lập màu cho các thẻ trong bảng.



























