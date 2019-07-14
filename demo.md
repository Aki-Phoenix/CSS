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