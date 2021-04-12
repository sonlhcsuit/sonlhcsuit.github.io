---
title: "Variable"
description: "Javascript variables, namebindings, lexical, etc."
date: 2021-04-12T19:01:17+07:00
draft: false
slug: "variable"
categories:
    - Programming Language
tags:
    - Javascript
image: cover.png
---

## Variable
Biến là một khái niệm rất quan trọng trong nhiều ngôn ngữ lập trình, được sử dụng để lưu trữ cá giá trị. Chúng ta có thể gán một giá trị cho một biến, khi nào cần giá trị (số, chuỗi, etc) thì gọi tên biến thay vì giá trị, các *interpreter*, *compiler* truy xuất đến giá trị đã được gán vào biến khi thực hiện việc tính toán thay cho chúng ta. Con người dễ tiếp thu ngôn ngữ hơn là những giá trị, con số, biến là một ánh xạ đơn giản, từ *một từ* sinh ra *giá trị*. Tên của biến phải là độc nhất theo những quy tắc đặt tên của các ngôn ngữ lập trình, một biến chỉ lưu trữ một giá trị tại 1 thời điểm nhất định.

Thoát khỏi việc ghi nhớ các giá trị bằng cách sử dụng biến, các lập trình viên lại có thêm vài vấn đề như sau: Đặt tên biến như thế nào để ngắn gọn, dễ nhớ? Muốn nhiều biến có cùng tên được không? etc. Nhằm giải quyết vấn đề về *cách đặt tên biến*, các ngôn ngữ lập trình đã hỗ trợ thêm những khái niệm *lexical, scope,...* 

## Variable naming
Nói về việc đặt tên biến thì có nhiều quy tắc
- Tối thiểu:
    - Tên của một biến phải độc nhất trong một phạm vi nhất định
    - Bao gồm các ký tự trong bảng chữ cái (cả thường và hoa), số, ký tự đặc biệt cho phép tuỳ theo mỗi ngôn ngữ lập trình (JS thì chỉ cho phép 2 ký tự là "_" và "$")
    - Không được trùng với các reserved word (keyword)
    - Không được bắt đầu bằng số
- Có thể có :
    - Ít mang động từ
    - Ngắn ngọn, súc tích, có nghĩa 
    - Sử dụng cách nối (như kebab case, snake case, camel case,etc.) khi có nhiều hơn 2 từ
    - ...
Và quan trọng hơn hết là phải tuân thủ cú pháp để khai báo biến của ngôn ngữ lập trình!
```js
// ở trong javascript, chúng ta có 3 cách khai báo biến 
// bằng viêc sử dụng 3 reserved word như var, let, const
var revenues;
let costs;
const profits;
```

Vốn từ vựng nhiều là một lợi thế khi đặt tên biến, tuy nhiên chúng ta không đặt tên biến khác nhau hoàn toàn. Nếu đặt tên biến khác nhau hoàn toàn thì sẽ có rất nhiều biến, việc nhớ chúng sẽ rất tốn thời gian. Thay vì đó, các ngôn ngữ lập trình hỗ trợ các khái niệm *idetifier, scope, lexical,etc.* để giúp chúng ta tiết kiệm thời gian, công sức.

## Identifier & access scope
Biến là một **identifier**, tức là định danh (identifier còn có thể các function, class,etc). Chúng ta có thể khởi tạo (tạo ra) nhiều biến có cùng tên, lưu trữ các giá trị khác nhau ở các **scope** khác nhau. Trình duyệt sẽ dựa vào các scope, xác định các **identifier** và giá trị của chúng phù hợp. Các **identifier** khi được khởi tạo luôn được gắn chặt với **scope** nơi mà chúng được khởi tạo. Chúng ta chỉ có thể truy cập tới các identifier ở các **outer scope**, không đối với **inner scope**. **Scope** có phạm vi truy cập lớn nhất **Global Scope**. Sự khác biệt giữa **let** & **var**

```js
let revenues = 100000;
let costs = 12345
if (revenue > 0 ){
  let profits = revenues - costs

}
console.log(profits)
// ReferenceError: profits is not defined
// Hàm console ở global scope truy cập tới biến profits, 
// tuy nhiên biến profits được khởi tạo ở scope của if (inner scope), 
// nên việc truy cập thất bại. Tuy nhiên việc truy cập 
// revenues & costs đều thành công khi ở trong scope của if vì 
// đối vời scope của if thì global là outer scope
```
Khi thực hiện việc tìm kiếm các **identifier** thì ta sẽ tuân theo quy tắc từ trong ra ngoài. Javascript sẽ xét ở scope hiện tại, sau đó chuyện tới outer scope, xét tiếp, tiếp tục chuyển tới outer scope,... cho tới khi gặp được **identifier** hợp lệ hoặc tới global scope mà không tìm được thì sẽ báo lỗi - scopes chain. Đối với từ khoá `let` thì quy tắc **scopes chain** đúng hoàn toàn, và nhiều ngôn ngữ khác cũng vậy. Tuy nhiên điều này không đúng với `var`.

```js
if (true){
  var z = 100
}
console.log(z)
// 100 
// Điều này chứng mình rằng khi khai báo var, quy tắc scope chain
// không còn chính xác nữa
```

`var` đặc biệt hơn với `let` ở chỗ nó không tuân theo quy tắc chung. Chúng ta có thể kết luận rằng, khi khai báo **identifier** với từ khoá `var` sẽ có scope là global không? Tất nhiên là không!

```js
function initialVariable() {
  var z = 'this is z'
  console.log(z)
}
initialVariable()
console.log(z)
// this is z
// ReferenceError: z is not defined
```

Vậy nên ta không thể kết luận rằng **khai báo identifier với từ khoá `var` sẽ có scope là global**. Vậy thì lí do tại sao ví dụ ở trên lại bị sai nhỉ? Câu trả lời là đối với **scope** của hàm thì có một chút khác biệt, có tên là **lexical**. Khi khai báo **identifier** bằng `var`, thay vì **bind** vào scope, thì **identifier** được **bind** vào **lexical**. Ngoại trừ điều đó ra thì `var` còn có khả năng **redeclarion** (tái khai báo) mà không gặp lỗi. (làm với `let` thì sẽ gặp lỗi `SyntaxError: Identifier _ has already been declared`)
```js
var z ='this is z at first'
console.log(z)
function initialVariable() {
  var z = 'this is z'
  console.log(z)
  var z = 'this is z but 4th' // redeclaration
  console.log(z)
}
initialVariable()
console.log(z)
// this is z at first
// this is z
// this is z but 4th
// this is z at first
```
Xét thêm trường hợp này 
```js
var z= 1000
function f() {
  var fs = []
  for (var i = 0; i < 5; i++) {
    fs.push(function () {
      var z = i
      console.log(z)
    })
  }
  fs[3]()
}
f()
console.log(z)
// 5
// i được khai báo ở lexical f, khi thực hiện vòng lặp với post operator là i++ thì 
// đang thay đổi giá trị của biến i ở lexical f. 
```
Ngoại trừ việc **bind** khác một chút `var` vẫn tuân theo quy tắc của **scope chain**. Có nhiều bạn tưởng rằng `var` sẽ tạo một property ở global object (cụ thể window ) - Nhưng thực sự không phải vậy. chỉ khi nào bạn khai báo bằng `var` ở global scope thì mới tạo property, còn lại thì không.
```js
function f() {
    var z = '111'
    console.log(z)
    console.log(window.z)
}
f()
```

## `const`
Điều khiến **identifier** đặc biệt là không cho phép **direct assignment**. Assignment là một toán tử cho phép cập nhật **giá trị** đã được lưu trữ của **identifier**.

```js
const z = 100;
z = '??'
// TypeError: Assignment to constant variable.
```
Tuy nhiên ,việc thay đổi nội tại bên trong, hoặc thay đổi thông qua trung gian vẫn có thể.(Đối với references data type)
```js
const z = []
console.log(z)
z.push(1,2,3,4)
console.log(z)
// []
// (4) [1, 2, 3, 4]
```
```js
const z = {}
z.name = 'z'
console.log(z)
// {name: "z"}
```

<!-- ## Hoisting & TDZ -->

---
# References & more resources
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference
