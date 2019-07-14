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
 