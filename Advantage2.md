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