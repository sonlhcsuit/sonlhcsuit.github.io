---
title: "Javascript Prototype"
description: "How Javascript implements OOP in details"
date: 2021-07-25T21:32:38+07:00
draft: true
math: false
slug: "javascript-prototype"
categories:
    - Javascript
categories:
    - programming-language
image: cover.png

---

# Javascript & OOP
Trước khi trình bày cụ thể về cách mà Javascript triển khai OOP, các bạn có thể tham khảo bài viết trước của mình có trình bày sơ bộ về các cách triển khai OOP (gồm class-based & prototype-based)

Vốn dĩ từ ban đầu Javascript được tạo ra với mục đích chính là hướng mọi người tới với Functional Programming, nên trong những phiên bản đầu tiên của Javascript thì không có khái niệm class (vì Javascript đâu có phải Java), nhưng vật đổi sao dời thì những nhà phát triển đã nhận ra OOP là một **phát minh quan trọng không thể thay thế**. Nên các nhà phát triển Javascript đã dần dần cài đặt thêm các chức năng hỗ trợ **hướng đối tượng** vào Javascript. Để giữ tình mềm dẻo, linh hoạt của Javascript thì sự lựa chọn Prototype là an toàn nhất.

# Everything is Object
Có một câu nói về Javascript thế này : "Everything is an object, or a primitive". Về cơ bản thì mọi thứ ở trong Javascript đều là object (object trong object oriented programming), ngoại trừ một vài thứ khác như là: number, strings, null, undefined, boolean, symbols.

Để hiểu một cách đơn giản thì object trong Javascript giống như một hash map, một mapping **k**ey sang **v**alue. Chúng ta có thể truy cập đến value thông qua một key unique. Chúng ta có thể dễ dàng truy cập tới các phần tử mà object lưu trữ thông qua key và dot notation (toán tử .)

# Encapsulation 
Nói về hướng đối tượng, tính đóng gói được đặt lên hàng đầu đối với các ngôn ngữ định hướng đối tượng. Tuy nhiên Javascript làm điều này rất linh hoạt và loosely (lỏng lẻo). Với Java, tính đóng gói được thể hiển ở việc định nghĩa một class.

```java
public class Human {
    private String firstName;
    private String lastName;
    private int age;
    constructor(String firstName,String lastName,int age){
        this.firstName = firstName;
        this.lastName = lastName;
        this.age = age;
    }

    public void speak(){
        System.out.println('I am Human');
    }
}
```
Một object được tạo ra từ class Human sẽ chỉ có quyền truy cập tới những attributes & method có access modifier là public mà thôi. Còn đối với Javascript thì khái niệm access modifier có lẽ là không tồn tại, bởi vì: 
- Everything is objet
- Everykey in object is public

Đối với Javascript, ta có thể gọi class là một template thì chính xác hơn là một class, chúng ta có thể khai báo một template theo 2 cách.
```js 
function createHuman(firstName,lastName,age){
    let obj = {}
    obj.firstName = firstName
    obj.lastName = firstName
    obj.age = age
    obj.speak = function (){
        console.log(`I am Human, you can call me ${obj.firstName}`)
    }
    return obj
}
```
Tuy nhiên cách này lại có vẻ mất tự nhiên và hơi dài dòng, thay vào đó Javascript cũng hỗ trợ phiên bản xịn xò hơn để có thể ít viết code lại nhờ vào từ khoá `this` và toán tử `new` đi kèm với tên của class được viết hoa chữ cái đầu (mà không phải sử dụng tên hàm). Lúc này thì chúng ta có thể xem đây là một constructor (Javascript còn có cả từ khoá `class`)
```js 
function Human(firstName,lastName,age){
    this.firstName = firstName
    this.lastName = firstName
    this.age = age
    this.speak = function (){
        console.log(`I am Human, you can call me ${this.firstName}`)
    }
}
let human = new Human('Harry','Potter',18)
let human_ex = new Human('Hermione','Granger',18)
human.speak()
human_ex.speak()
// I am Human, you can call me Harry
// I am Human, you can call me Hermione
```
Cách thứ 2 thì lại ít được sử dụng hơn
---
# References & more resources


- https://kipalog.com/posts/prototype-la-khi-gi-
### P/S:
Nếu có gì sai sót xin gửi email cho mình để cập nhật, xin cảm ơn!
