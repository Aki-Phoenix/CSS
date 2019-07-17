CSS Advantage
1. CSS Rounded Cornes: Thuộc tính bo tròn đường viền
boder-radius: giá trị;

Có 4 loại: border-top-left-radius, border-top-right-radius, border-bottom-right-radius, border-bottom-left-radius...
Thuộc tính border-radius có thể có từ 1 đến 4 giá trị như:

- Four value-border-radius: 20px 50px 30px 10px;
    (bao gồm top-left, top-right, bottom-right, bottom-left)

    ```
    #Rounded_Cornes4{
    border-radius: 20px 50px 30px 10px;
    }
    ```

- Three value-border-radius: 20px 50px 30px;
    (bao gồm top-left, top-right = bottom-left, bottom-right) 

    ```
    #Rounded_Conrnes3{
    border-radius: 20px 50px 30px;
    }
    ```

 - Two value-border-radius: 20px 40px;
    (bao gồm top-left=bottom-right, top-right=bottom-left )

    ```
    #Rounded_Conrnes2{
    border-radius: 20px 40px;
    }
    ```

 - One value-border-radius: 20px;
    ( 4 góc bằng nhau)

    ```
    #Rounded_Conrnes1{
    border-radius:20px;
    }
    ```

2. CSS Border Images

Cho phép bạn chỉ định 1 hình ảnh sẽ được sử dụng thay vì đường viền thông thương sung quanh 1 phần tử. Ta cần xác định
- Hình ảnh được sử dụng làm đường viền
- Vị trí giá trị, vị trí cắt hình ảnh
- Xác định các phần ở giữa sẽ là lặp lại hay kéo dài

Để hình ảnh viền hiển thị, phần tử xác định cần thuộc tính `border`.

```
#borderimg{
border: 10px solid transparent; //transparent là thuộc tính chỉ độ trong suốt, giống với opacity
border-image: url(abc.png) 30 round; // round là lặp lại, stretch là kéo dài.
}
```

Với các giá trị vị trí cắt (slice) khác nhau ta nhận được được đường viền hoàn toàn khác nhau:

```
#borderimg_demo{
border: 10px solid transparent;
border-image: url(abc.png) 10% round;
}
```

Ta có thể sử dụng một số thuộc tính về Border Image như sau:

 - border-image-source: chỉ định cách cắt hình ảnh viền
 - border-image-width: chỉ định độ rộng của hình ảnh viền
 - border-image-outset: Chỉ định số lượng mà vùng hình ảnh viền vượt ra ngoài hôpj viền(border box)
 - border-image-repeat: Chỉ định hình ảnh viền sẽ được lặp lại(repeat), làm tròn(rounded) hoặc kéo dài(stretched).

 *cần hỏi lại*

3. CSS Multiple Backgrounds

- CSS cho phép người dùng thêm nhiều ảnh nền cho 1 thành phần thông qua thuộc tính background-image.

 - Các hình nền khác nhau được phân tách bằng dấu phẩy và các hình ảnh được xếp chồng lên nhau, ảnh đầu tiên gần với người xem.

```
#background_image{
backgroungd-image: url(abc.gif), url(cde.gif);
background-position: left top, right bottom;
background-repeat: no-repeat, repeat;
}
```

hoặc gọn hơn:

```
#background_image2{
background: url(abc.gif), url(cde.gif);
background-position: left top, right bottom;
background-repeat: no-repeat, repeat;
}
```

 - Ví dụ trên ta có nền sẽ là 2 hình ảnh abc.gif và cde.gif được sắp xếp lần lượt là trên cùng bên trái và dưới cùng bên phải, với ảnh thứ nhất sẽ không được lặp lại, và ảnh thứ 2 thì được lặp lại.


- Xác định kích thước cho ảnh nền:

```
#define_size1{
background: url(aa.gif);
background-size: 250px 100px;
}
```

- Ta có thể xác định kích thước của nhiều ảnh nền, thuộc tính `background-size` cũng chấp nhận nhiều giá trị cho kích thước các ảnh nên, kích thước các ảnh được phân cách bởi dấu `,` .

```
#define_size{
background: url(abc.gif), url(cde.gif), url(aaa.gif);
background-size: 100px,250px,auto;
}
```

- Ngày nay nhiều người muốn đặt hình nền cho website, hình nền được đặt ở giữa, lấp đầu toàn bộ trang web, chia tỉ lệ hình ảnh khi cần thiết, không gây ra thanh cuộn, ta có thể sử dụng đoạn code sau:

```
#full_background{
background: url(aaa.gif) center fixed;  //cần note//
background-repeat: no-repeat;
background-size:cover;
}
```

- Thuộc tính `background-origin`:

Chỉ định vị trí của hình nền. Nó có 3 giá trị:
 - border-box: hình nền bắt đầu từ góc trên bên trái của đường viền.
 - padding-box: (mặc định) hình nền bắt đầu từ góc trên bên trái tính từ padding
 - content-box: hình nền bắt đầu từ góc trên bên trái, có cách 1 khoảng bằng padding.

 ```
 #example1 {
  border: 10px solid black;
  padding: 35px;
  background: url(img_flwr.gif);
  background-repeat: no-repeat;
}

#example2 {
  border: 10px solid black;
  padding: 35px;
  background: url(img_flwr.gif);
  background-repeat: no-repeat;
  background-origin: border-box;
}

#example3 {
  border: 10px solid black;
  padding: 35px;
  background: url(img_flwr.gif);
  background-repeat: no-repeat;
  background-origin: content-box;
}
 ```

- Thuộc tính `background-clip`:

Chỉ định vùng vẽ của nền. Nó có 3 giá trị:
 - border-box: (mặc định) nền được vẽ ra cạnh ngoài của đường viền.
 - padding-box: (hay dùng) nền được vẽ ra cạnh ngoài của phần padding
 - content-box: nền được vẽ bên trong hộp nội dung.

 ```
 #example1 {
  border: 10px dotted black;
  padding:35px;
  background: yellow;
}

#example2 {
  border: 10px dotted black;
  padding:35px;
  background: yellow;
  background-clip: padding-box;
}

#example3 {
  border: 10px dotted black;
  padding:35px;
  background: yellow;
  background-clip: content-box;
}
 ```

 4. CSS Color
RGBA Colors: là phần mở rộng của giá trị màu RGB với alpha- chỉ định độ mờ cho màu.

Giá trị màu RGBA được chỉ định bẳng: rgba(red, green, blue, alpha). Tham số alpha là một số trong khoảng 0.0(hoàn toàn trong suốt) và 1.0(hoàn toàn mờ)

`rgba(255,0,0,0.2); `
`rgba(255,0,0,0.8); `

HSL Color: viết tắt của Hue, Saturation và Lightness.

Giá trị màu HSL được chỉ định bằng: hsl (hue-màu sắc, saturation-độ bão hòa, lightness-độ sáng).

Trong đó: 
- Hue là 1 độ trên bánh xe màu(từ 0->360)
 - 0(hoặc 360) là màu đỏ.
 - 120 là màu xanh
 - 340 là màu xanh
- Saturation là 1 giá trị phần trăm:
 - 100% là màu đầy đủ
- Lightness là 1 giá trị phần trăm:
 - 0% là màu tối(đen) và 100% là màu trắng.

 `hsl(0,100%,50%)`

Giá trị màu HSLA là phần mở rộng của HSL với alpha-chỉ định độ mở cho màu.

Giá trị của màu HSLA là: hsla(hue-màu sắc, saturation-độ bão hòa, lightness-độ sáng, alpha) trong đó alpha xác định độ mờ, là 1 số nằm trong khoảng 0.0(fully transparent-hoàn toàn trong suốt) và 1.0(full opaque-hoàn toàn mờ).

`hsla(0, 100%, 40%, 0.4)`

Opacity

Thuộc tính `opacity` trong CSS được sử dụng để chỉ độ mờ cho toàn bộ thành phần(bao gồm background và text sẽ mờ/trong suốt)

Thuộc tính `opacity` có giá trị là một số nằm trong khoảng 0.0(full transparent) và 1.0(fully opaque).

```
#demo{
background-color: rgb(255,0,0); 
opacity:0.6;
}
```

 CSS Gradients: cho phép bạn hiển thị các hiệu ứng chuyển tiếp mượt mà giữa hai hoặc nhiều màu được chỉ định.

 Để tạo ra 1 CSS Gradients ta cần xác định 2 yếu tố:

  - Linear Gradients-độ dốc tuyến tính (đi xuống/lên/trái/phải/chéo)
  - Radial Gradients(được xác định bởi trung tâm của họ)

  CSS Linear Gradients

  Để tạo 1 linear gradients ta cần xác định ít nhất hai điểm dừng màu. Điểm dừng màu là màu ta muốn hiển thị chuyển tiếp mượt mà. Ta có thể đặt điểm bắt đầu và hướng(hoặc góc) cùng với hiệu ứng chuyển màu.

  Cú pháp: 
  ```
  background-image: linear-gradient(direction, color-stop1, color-stop2,....)
  ```

  Linear Gradient - Top to Bottom(mặc định)

  Đây là hiệu ứng chuyển tiếp màu từ trên xuống dưới.

  ```
  #example{
  background-image:linear-gradient(blue, violet);
  }
  ```

  Linear Gradient - Left to Right

  Hiệu ứng chuyển tiếp màu từ trái qua phải.

  ```
  #example2{
  background-image: linear-gradient(to right, red, yellow);
  }
  ```

  Linear Gradient - Diagonal

  Hiệu ứng chuyển tiếp màu theo đường chéo từ trên xuống dưới.

  ```
  #example3{
  background-image: linear-gradient(to bottom, blue, white);
  }
  ```

  Chuyển tiếp màu sử dụng góc:

  Góc được chỉ định là một góc giữa một đường ngang và đường dốc-linear gradient

  ```
  background-image: linear-gradient(angle-góc, color1, color2);
  ```

 ```
 #example4{
   background-image: linear-gradient(-90deg, red, yellow);
 }
 ```

 Sử dụng nhiều màu dừng

 ```
 #exam{
  background-image: linear-gradient(red, yellow, green);
 }
 ```

```
#exam2{
  background-image: linear-gradient(to right, red, blue, orange, violet, yellow);
}
```
CSS gradient cho phép sử dụng thuộc tính transparency(độ trong suốt) để tạo hiệu ứng mờ dần.

Để thêm hiệu ứng trong suốt ta sử dụng hàm rgba() để xác định các điểm dừng màu. Tham số cuối của rgba() chỉ độ trong suốt từ 0->1(không trong suốt)

```
#exam{
  background-image: linear-gradient(to right, rgba(240,0,0,0), rgba(240,0,0,1));

  //màu được chuyển dần ban đâu flaf trong suốt đến màu chuẩn rgba(240,0,0,1)
}
```

Lặp lại một linear-gradient

```
#exam{
  background-image: repeating-linear-gradient(red, yellow 10%, green 20%);
  }
}
```

CSS Radial Gradient....





 