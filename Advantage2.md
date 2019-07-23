5. CSS Shadows
- Shadows Effects( Hiệu ứng bóng)

Ta có thêm hiệu ứng bóng cho văn bản và bên ngoài các phần tử khác. Đặc trung có 2 thuộc tính:

 - Text-shadow: được sử dụng cho văn bản, ta cần xác định bóng ngang và bóng dọc.

 ```
 h1{
    text-shadow: h-shadow v-shadow blur-radius color;
 }
 ```

 Trong đó: 
  - h-shadow: vị trí bóng ngang so với chữ, số âm sẽ đẩy lên và số dương sẽ đẩy xuống.
  - v-shadow: vị trí bóng dọc so với chữ, số âm sẽ đẩy lùi phía sau và số dương sẽ đẩy tới phía trước.
  - blur-radius: độ nhòe của bóng chữ, tính bằng px.
  - color: màu sắc của bóng. 

 Ví dụ: Hiệu ứng bóng cho văn bản có màu xanh(blue) và độ mờ là 5px:

 ```
 example1{
     text-shadow: 3px 3px 5px blue;
 }
 ```

 Ta có thêm vào văn bản nhiều bóng, danh sách các bóng được phân tách bằng dấu phẩy.

 Ví dụ: Văn bản dưới đây sẽ có màu đỏ, có bóng ngang và dọc là 2px, và có màu bóng là màu vàng, màu xanh lam và màu xám.

```
example2{
    color: red;
    text-shadow: 1px 1px 2px yellow, 0px 0px 20px blue, 0px 0px 5px gray;
}
```

Ngoài ra, ta cũng có thể sử dụng thuộc tính `text-shadow` để tạo đường viền đơn giản xung quanh một số văn bản(không có bóng).

Ví dụ:
```
example3{
    color:yellow;
    text-shadow: -1 px 0 black, 0 1px black, 1px 0 black, 0 -1px black
}
```

 - Box-shadow: Thuộc tính áp dụng bóng cho viền bên ngoài của phần tử, ta cũng cần xác định bóng ngang và bóng dọc.

 ```
 h1{
     box-shadow: h-shadow v-shadow blur spread color;
 }
 ```

 Trong đó:
  - h-shadow: vị trí bóng ngang so với chữ/viền, số âm sẽ đẩy lên, số dương đẩy xuống.
  - v-shadow: vị trí bóng dọc so với chữ/viền, số âm sẽ đẩy lui phía sau và số dương sẽ đẩy tới phía trước.
  - blur-radius: độ nhòe.
  - spread: kích thước của bóng.
  - color: màu của bóng

  Ví dụ:

  ```
  #example4{
      box-shadow: 1px 2px 4px rgba(0,0,0, 0.5);
  }
  ```

Ta cũng có thể sử dụng `box-shadow` để tạo thẻ:

```
#card{
    width:250px;
    box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);
    text-align:center
    //tham khảo thêm trên w3school
}
```

6. CSS Text Effects (hiệu ứng văn bản)

- CSS Text Overflow: Thuộc tính chỉ định cách thức nội dung tràn không được hiển thị sẽ được báo hiệu cho người dùng.

Nội dung tràn sẽ bị cắt bớt khi hiển thị nếu ta dùng `text-overflow: clip`

```
#test1{
    overflow:hidden;
    text-overflow:clip;
}
```

Hoặc nội dung tràn sẽ được hiển thị bằng dấu `...` nếu ta dùng `text-overflow:ellipsis`

```
#test2{
    overflow:hidden;
    text-overflow:ellipsis;
}
```

Hiển thị nội dung tràn khi di chuột qua phần tử ta dùng:  `:hover` kết hợp với `overflow:visible`

```
test3:hover{
overflow:visible
}
```

- CSS Word Wrapping: Thuộc tính cho phép các từ dài có thể bị phá vỡ và gói vào dòng tiếp theo.

Nếu 1 từ quá dài để vừa tròn 1 khu vực, nó sẽ mở rộng ra bên ngoài, ta có thể dùng `word-wrap` để buộc văn bản phải bọc lại. Không cho nó tràn khỏi khu vực quy định, dù các từ có phải tách ra để xuống dòng.
```
#wrap1{
    word-wrap: break-word;
}
```

- CSS Word Breaking: Thuộc tính chỉ định quy tắc ngắt dòng.
 - `word-break: keep-all` Ngắt dòng theo chữ, không bị cắt chữ.

 ```
 #break1{
    width: 140px; 
    border: 1px solid #000000;
    word-break: keep-all;
 }
 ```

 - `word-break: break-all` Ngắt dòng khi không đủ chỗ, bị cắt cữ nếu thiếu chỗ.
 ```
 #break2{
    width: 140px; 
    border: 1px solid #000000;
    word-break: break-all;
 }
 ```

- CSS Writing Mode: Thuộc tính chỉ định liệu các dòng băn bản được đặt theo chiều ngang hay chiều dọc.
 - `writing-mode: horizontal-tb` chữ viết ngang(mặc định).
 ```
 test1 {
  writing-mode: horizontal-tb; 
}
 ```

 - `writing-mode: vertical-rl` chữ viết theo chiều dọc
 ```
 p.test2 {
  writing-mode: vertical-rl; 
}
 ```

7. CSS Web Font

Quy tắc sử dụng phông chữ: Được xác định trong CSS `@font-face` 

Các định dạng phông chữ khác nhau:
- TrueType Fonts(TTF): Là một tiêu chuẩn phông chữ được phát triển vào cuối những năm 1980, bởi Apple và Microsoft. TrueType là định dạng phông chữ phổ biến nhất cho cả hệ điều hành Mac OS và Microsoft Windows.

- OpenType Fonts(OTF): Là một định dạng cho phông chữ m áy tính có thể mở rộng. ó được xây dựng trên TrueType và là nhãn hiệu đã đăng kí của Microsoft. Phông chữ OpenType được sử dụng phổ biến hiện nay trên các nên tảng máy tính chính.

- The Web Open Font Format(WOFF): Là một định dạng cho phông chữ được sử dụng trên các trang web. Được phát triển vào năm 2009. WOFF về cơ bản là OpenType hoặc TrueType với nén và siêu dữ liệu bổ sung. Mục tiêu là hỗ trợ phân phối phông chữ từ máy chủ đến máy khách qua mạng với các ràng buộc về băng thông.

- WOFF 2.0: Phông chữ TrueType/ OpenType cung cấp khả năng giải nén tốt hơn WOFF 1.0.

- SVG Fonts/Shapes: //note

- Embedded OpenType Fonts(EOT): Là một dạng phông chữ OpenType nhỏ gọn được Microsoft thiết kế để sử dụng làm phông chữ nhúng trên các trang web.

Sử dụng font chữ mình muốn, trong quy tắc `@font-face` ta xác định tên phông chữ, và sau đó là trỏ đến tệp phông chữ. Để sử dụng phông chữ cho 1 phần tử HTML, ta sử dụng thuộc tính`font-family`:

```
//cài đặt phông chữ
@font-face{
    font-family: FontFreak;  //tên font là FontFreak
    src: url(fontfreak.woff/) // địa chỉ tệp phông chữ
}
//áp dụng phông chữ đã cài đặt cho đối tượng trong thẻ div
div { 
    font-family: FonFreak;
}
```

Sử dụng chữ đậm: Ta phải thêm 1 quy tắc khác trong `@font-face` có chứa các mô tả cho văn bản in đậm:

```
@font-face{
    font-family: FontFreak;
    src: url(fontfreak_bold.woff); //tệp này là 1 tệp phông chữ khác có chứa các kí tự in đậm cho phông chữ fontfreak
    font-weight: bold;
}
```

Các mô tả phông chữ có thể được xác định bên trong `font-face`:
 - font-family: name;
 - src: URL;
 - font-stretch: normal/condensed/ultra-condensed/extra-condensed/semi-condensed/expanded/semi-expanded/extra-expanded/ultr-expanded.
 - font-style: normal/italic/oblique
 - font-weight: normal/bold/100/200/...

8. CSS 2D Transforms

CSS Transforms cho phép người dùng di chuyển, xoay, chia tỷ lệ và các phần tử nghiêng. 

Các phương thức chuyển đổi 2D:
- translate(): Là Phương pháp di chuyển một phần tử từ vị trí hiện tại của mình(theo các thông số đưa ra cho các trục X và trục Y)

```
div{ //di chuyển phần tử trong thẻ <div> 50px sang phải và giảm 100px từ vị trí hiện tại của nó.
    transform: translate(50px, 100px);
}
```

- rotate(): Là phương pháp quay một chiều kim đồng hồ, hoặc truy cập chiều kim đồng hồ theo một mức độ nhất định. Khi sử dụng giá trị âm phần tử sẽ xoay ngược chiều kim đồng hồ.

```
div2{ // xoay phần tử trong thẻ <div> theo chiều kim đồng hồ 1 góc 30 độ.
    transform: rotate(30deg);
}
```

- scale(): Là phưphần tử(theo các thông số đứa ra cho ơng pháp tăng hoặc giảm kích thước của 1 chiều rộng và chiều cao).

```
div3{ //tăng phần tử trong thẻ div gấp 2 lần chiều rộng và gấp 3 lần chiều cao ban đầu của nó.
    transform: scale(2,3);
}
div4{ //giảm chiều rộng và chiều cao xuống một nửa.
    transform: scale(0.5,0.5);
}
```

- scaleX(): Là phương pháp tăng hoặc giảm chiều rộng của một phần tử.

```
div4{ //tăng chiều rộng gấp 2 lần.
    transform: scaleX(2);
}
div5{ //giảm chiều rộng xuống một nửa.
    transform: scaleX(0.5);
}
```

- scaleY(): Là phương pháp tăng hoặc giảm chiều cao của một phần tử.

```
div6{ // tăng chiều cao lên gấp 3 lần.
    transform: scaleY(3);
}
div7{ //giảm chiều cao xuống một nửa.
    transform: scaleY(0.5);
}
```

- skewX(): là phương pháp làm lệch một yếu tố dọc theo trục X bởi các góc độ nhất định.

```
div{ // làm nghiêng 1 thẻ <div> một góc 30 độ dọc theo trục X.
    transform: skewX(30deg);
}
```

- skewY(): Là phương pháp làm lệch một yếu tố dọc theo trục Y bởi góc độ nhất định.

```
div{ // làm nghiêng phần tử <div> một góc 30 độ dọc theo trục Y.
    transform: skewY(30deg);
}
```

- skew(): là phương pháp làm lệch một yếu tố dọc theo trục X và trục Y bởi những góc nhất định. Nếu tham số thứ 2 không được xác định nó sẽ mặc định bằng 0.

```
div{ //làm nghiêng phần tử <div> một góc 30 độ dọc theo trục X và 50 độ dọc theo trục Y.
    transform: skew(30deg, 50deg)
}
```

- matrix(): Là phương pháp kết hợp tất cả các phương pháp chuyển đổi 2D thành một. Nó có các tham số như sau:

`matrix(scaleX(), skewY(), skewX(), scaleY(), translateX(), translateY())`

```
div{
    transform: matrix(1, -0.3, 0, 1, 0, 0);
}
```

9. 3D Transforms

Các phương thức chuyển đổi:
- rotateX(): Là phương pháp quay một yếu tố xung quanh trục X của nó ở một mức độ nhất định.

```
#exam{
    transform: rotateX(180deg);
}
```

- rotateY(): Phương pháp quay một yếu tố xung quanh trục Y của nó ở một góc nhất định.

```
#exam{
    transform: rotateY(90deg);
}
```

- rotateZ(): Phương pháp quay một yếu tố xung quanh trục Z của nó ở một mức độ nhất định.

```
#exam{
    transform: rotateZ(90deg);
}
```

10. CSS Transitions

Cho phép thay đổi giá trị thuộc tính một cách trơn tru, trong một khoảng thời gian nhất định.

- transition-timing-function: quy định các đường cong tốc độ của hiệu ứng chuyển tiếp.

Nó có các giá trị như sau:
 - ease: Chỉ định hiệu ứng chuyển tiếp với khởi đầu chậm, sau đó nhanh, sau đó kết thúc chậm(mặc định).
 - linear: Chỉ định hiệu hứng chuyển tiếp với cùng tốc độ từ đầu đến cuối.
 - ease-in: Chỉ định hiệu ứng chuyển tiếp với khởi đầu chậm.
 - ease-out: Chỉ định hiệu ứng chuyển tiếp với kết thúc chậm.
 - ease-in-out: Chỉ định hiệu ứng chuyển tiếp với khởi đầu và kết thúc chậm.
 - cublic-bezier(n,n,n,n): Cho phép xác định các giá trị của riêng mình trong hàm cublic-bezier.

- transition-delay: Quy định cụ thể một giá trị delay(tính bằng giây) cho các hiệu ứng chuyển.

- transition-duration: Cho phép chỉ định thời gian hoàn thành 1 hiệu ứng chuyển tiếp(s/mms).
- transition-property: Chỉ định tên của thuộc tính CSS, hiệu ứng chuyển tiếp dành cho nó.

11. CSS Animations

CSS cho phép các phẩn tử HTML hoạt động liên tiếp mà không cần sử dụng Javascrip hoặc Flash.

Ta tìm hiểu các thuộc tính như:
- @keyframes: Khi chỉ định kiểu CSS bên trong `@keyframes` hình động sẽ thay đổi từ kiểu hiện tại sang kiểu mới vào những thời điểm nhất định.

```
@keyframes exam{ //chỉ định hiểu thay đổi bằng từ khóa `from` và `to` đại diện cho 0%(bắt đầu) và 100%(hoàn thành).
    from {background-color: red;}
    to {background-color: yellow;}
}
div{
    width:100px;
    height: 100px;
    background-color:red;
    animation-name: exam; //tên của animation.
    animation-duration: 4s; // xác định thời thời gian hình ảnh động cần thực hiện để hoàn thành. Nếu không chỉ định thời gian, sẽ không có hình ảnh động.
}
```
- animation-delay: Quy định sự chậm trễ cho dự bắt đầu của một hình ảnh động.

```
div { //trễ 2s trước khi hình bắt đầu hoạt động
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-delay: 2s; // nếu để giá trị âm (-N), sẽ được hiểu là hình đã hoạt động được N giây.
}
```
- animation-iteration-count: Thuộc tính sác định số lần chạy trước khi dừng của hình động.

```
div { //hình sẽ chạy 5 lần trước khi dừng.
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: 5; //sử dụng `infinite` nếu muốn hình chạy mãi.
}
```
- animation-direction: Quy định hình động được phát theo chiều nào. Nó có các giá trị:
 - normal: Hình được phát như bình thường(default).
 - reverse: Hình được phát theo hướng ngược lại.
 - alternate: Hình được phát bình thường trước sau đó phát ngược lại.
 - alternate-reverse: Hình được phát ngược trước sau đó phát như bình thường.

- animation-timing-function: Chỉ định đường cong tốc độ của ảnh động. Nó có các giá trị sau:
 - ease: Chỉ định ảnh động bắt đầu với khởi đầu chậm, sau đó nhanh, sau đó kết thúc chậm(default).
 - linear: Chỉ định ảnh động có cùng tốc độ từ đầu đến cuối.
 - ease-in: Chỉ định ảnh động với khởi đầu chậm.
 - ease-out: Chỉ định ảnh động có kết thúc chậm.
 - ease-in-out: Chỉ định ảnh động với khởi đầu và kết thúc đều chậm.
 - cublic-bezier(n,n,n,n): Cho phép xác định các giá trị riêng của mình trong hàm cublic-bezier.

- animation-fill-mode: Quy định cụ thể một phong các cho các phần tử mục tiêu khi ảnh đọng không được phát (trước khi nó bắt đầu, sau khi nó kết thúc hoặc cả hai). Nó có các giá trị:
 - none: (default) Ảnh động sẽ không áp dụng bất kì kiểu nào cho thành phần trước hoặc sau khi nó được phát.
 - forwards: Phần tử sẽ giữ lại các kiểu giá trị được đặt bởi khung hình chính cuối cùng(tùy thuộc vào hướng đi và số lần lặp lại của ảnh động).
 - backwards: Phần tử sẽ nhận các kiểu giá trị được đặt bởi khung hình chính đầu tiên(phụ thuộc vào hướng đi của ảnh động).
 - both: Ảnh động sẽ tuân thủ theo các quy tắc cho cả tiến và lùi, mở rộng các thuộc tính ảnh động theo cả 2 hướng. 

- animation: Là thuộc tính ngắn gọn cho phép người dùng chị định các giá trị cho các thuộc tính trong đối với ảnh động.

`animation: exam 5s linear 2s infinite alternate;`

Trong đó:
 - exam: animation-name
 - 5s: animation-duration
 - linear: animation-timing-function
 - 2s: animation-delay
 - infinite: animation-iteration-count
 - alternate: animation-direction