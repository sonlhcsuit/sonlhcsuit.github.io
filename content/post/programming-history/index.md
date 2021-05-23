---
title: "Programming Language History Overview"
description: "Programming Language history & relevants concepts" 
date: 2021-05-04T08:21:25+07:00
draft: false
math: true
slug: "programming-language-overview"
categories:
    - programming-language
    
image: cover.png

---

# History about Programming Languages & Computer

Chúng ta có thể khái quát lịch sử máy tính bằng bài viết khác, nhưng sau thời gian dài phát triển, thì công dụng chủ yếu của máy tính là để tính toán dựa trên *input* và sinh ra *output*. Máy tính ở thời điểm ban đầu có kích thước rất to (lớn hơn $100 m^2$), vật đổi sao dời khiến kích thước máy tính giảm dần bởi **CPU** (*Central Processing Unit*) - lõi của máy tính càng ngày càng nhỏ dựa vào công nghệ *nano*. Thời điểm ban đầu, **CPU** được chế tạo dựa trên bóng đèn dây tóc - biểu thị trạng thái bật (số 0) và tắt (số 1). Công nghệ phát triển giúp chúng ta thay thế bóng đèn bằng bóng bán dẫn nhỏ hơn bóng đèn cả nghìn lần. Nhờ vào việc thay đổi sử dụng *transistor* (bóng bán dẫn) vào việc chế tạo, khiến cho kích thước **CPU** càng ngày càng nhỏ (dẫn tới hệ quả là kích thước máy tính nhỏ dần). Một định luật có tên là **Moore** phát biểu rằng, cứ sau một chu kỳ thời gian nhất định thì số lượng *transistor* trên một đơn vị diện tích ( $cm^2$ ) sẽ tăng gấp đôi. Công nghệ *nano* còn có nhiều không gian để phát triển, chu kỳ của **Moore's Law** là 2 năm (Đến thời gian hiện tại thì mình không dám chắc vì không biết rõ là công nghệ nano có thể đạt tới kích thước bao nhiêu. Theo thông tin tham khảo thì 1 *transistor* đạt kích thước 0.2 nanometer - $10^{-9}$ meter). Bởi vì lí do chỉ có thể sử dụng 2 trạng thái on/off (cho dòng điện chạy qua) của một bóng đèn / *transistor* nên máy tính chỉ hiểu được số nhị phân. Kết hợp các *transistor* và các mạch **logic** khiến cho **CPU** có thể thực hiện việc tính toán. Và **computer** được gọi là bởi **computer** bởi vì được sinh ra với mục đích là **compute**.

![Block Diagram of Computer](image-1.png)

**CPU** của máy tính được dựa trên những thành phần cơ bản gồm **ALU** (*Arithmetic & Logic Unit* - Bộ xử lý tính toán), **Main Memory** (Bộ nhớ chính), **CU** (**Control Unit** - Bộ điều khiển) và các thành phần khác như *cache*, *register*, et cetera. Chúng ta khiến **computer** thực hiện tác vụ bằng việc sử dụng **instructions set** ( bộ lệnh) phù hợp đã được định nghĩa sẵn bởi mỗi nhà thiết kế máy tính. Mỗi máy tính có một đặc điểm khác nhau về việc thiết kế kiến trúc, thiết kế của ALU khác nhau (cùng 1 việc thực hiện phép toán + nhưng có nhiều cách) dẫn tới việc **instructions set** cũng khác nhau. *Developer/scientist* thực hiện công việc xây dựng các chương trình hằng ngày bằng việc sử dụng **instructions set** bằng mã nhị phân. Điểm yếu của phương pháp này là **chương trình viết trên một máy tính sẽ không chạy trên máy tính khác kiến trúc**.

Các **instructions set** này còn được gọi là **machine language/binary language**, đây là loại ngôn ngữ lập trình sơ khai nhất. **Programming Language** (ngôn ngữ lập trình) được tạo ra bởi con người, được sử dụng nhằm mục đích giao tiếp với máy tính, khiến cho máy tính thực hiện các hành vi do người dùng (**developer/scientist**) chỉ định.

# Classification of Programming Language
Có rất nhiều cách để phân loại ngôn ngữ lập trình dựa trên nhiều tiêu chí. Một tiêu chí hay dùng nhất là dựa trên độ khó của việc viết: **low-level** & **high-level**, và nhiều tiêu chí khác, ta có thể loại sơ bộ nhất như sau :
- low-level:
    - machine langugage
    - assembly language
- high-level: gồm các paradigm sau.
    - structural language
    - procedural language
    - object oriented language
    - functional language

Ưu điểm của ngôn ngữ **low-level** rất rõ ràng: siêu nhanh, chạy trực tiếp trên **CPU**. Tuy nhiên yếu điểm cũng không kém cạnh: chỉ gồm bit 0 hoặc 1 (**machine code**) siêu khó đọc, siêu khó viết, dể ẩn tàng lỗi, siêu khó bảo trì. Một điểm mạnh để thay thế yếu điểm của **assembly code** so với **machine code** là có thể sử dụng **english word** (dễ nhớ) cải thiện code đáng kể, tuy nhiên thì vẫn phải làm việc với 0 và 1. Dù cải thiện nhiều yếu điểm, nhưng thực sự vẫn khó bắt đầu lập trình, và đặc biệt là không có cấu trúc rõ ràng, chỉ gồm một **list instructions**. Yêu cầu cần **assembler** để phiên dịch **assembly code** thành **machine code**. Tuy nhiên vẫn cần **assembler** khác nhau dành cho mỗi máy tính kiến trúc khác nhau.

Ưu của của ngôn ngữ **high-level** thì không cần ai phải bàn cãi: viết code một lần, dễ đọc, dễ hiểu, dễ debug (ít nhất là so với **assembly**), có thể chạy ở hầu hết loại máy tính. Câu lệnh tiếng anh rất dễ đọc và dễ viết, cung cấp khả năng trừu tượng. Yếu điểm là phải cần một **compiler/interpreter** khác nhau cho mỗi loại máy tính. Điều cần phải củng cố **compiler/interpreter** cho từng loại kiến trúc (x86,et cetera). Ưu điểm rất là rõ ràng, và đa phần **developer** sử dụng **high-level language** nên việc phân loại tiếp theo sẽ tập trung vào các **high-level language**. Lưu ý việc phân loại ở đây, không phải là phân loại từng ngôn ngữ lập trình mà là phân loại các **paradigm** (mô hình ngôn ngữ lập trình).

# Structural Programming & Procedural Programming
**Structured Programming** nghĩa là lập trình có cấu trúc, vậy thế nào là có cấu trúc? "Cấu trúc" ở đây nói về việc xử lý các dòng code một cách hợp lý bằng việc hỗ trợ thêm các khái niệm như: *blocks*/*scopes*, *control flows* (*condition* & *repitition*), *subroutines*. Tại sao lại hỗ trợ thêm các khái niệm này? Trước khi các khái niệm này sinh ra thì đa phần các chương trình đều viết bằng assembly nên việc sử dụng câu lệnh jump/goto là cực kỳ phổ biến. Hãy xem xét ví dụ về việc rẽ nhánh và lặp sau đây.

```asm
mov eax,1
cmp eax,3 ; how does eax compare with 3?
jl lemme_outta_here  ; if it's less, then jump
mov eax,999  ; <- not executed *if* we jump over it
lemme_outta_here:

ret
```

```asm
mov eax,0 ; sum added here
mov edi,4

start: ; loop begins here
add eax,10 ; add each time around the loop
sub edi,1 ; loop increment
cmp edi,0 ; loop test
jg start ; continue loop if edi>0

ret
```

Nhìn vào 2 ví dụ trên thì mọi chuyện không khác biệt, nếu bạn đã cố gắng hiểu những dòng *comment*. Tuy nhiên, khi debug *assembly code* thì thực sự là một cực hình (ít nhất thì mình có từng chạy *code assembly* khi học Computer Architecture - Kiến trúc máy tính), đặc biệt là phải soi rất kỹ lệnh `cmp` và lệnh `jump` các loại, đồng thời còn quan sát từng label nữa. Việc sử dụng câu lệnh goto sẽ khiến cho code chúng ta được tối ưu (không gian dòng lệnh, chức năng, tốc độ, et cetera) nhưng lại mang đến một hậu quả kinh khủng là cực hình khi debug (nhìn nhầm 1 dòng là không biết *instructions pointer* chạy đi đâu luôn). Để giải quyết vấn đề này thì một vài khái niệm đã xuất hiện giúp cho cuộc sống của các lập trình viên dễ dàng hơn bằng việc hỗ trợ thêm khái niệm scopes / control flows giúp code dễ đọc hơn khi phải thực hiện các thao tác như so sánh, lặp, hàm, et cetera. Hỗ trợ thêm nhiều từ khoá giúp con người dễ dàng làm quen hơn.

```cxx
int eax = 1;
if (eax < 3){
    eax = 999;
}
```

```cxx
int eax = 1;
int edi = 4;
while (edi > 0){
    eax = eax + 10;
    edi = edi - 1;
}
```

Bàn về **procedural programming**, cơ bản là mở rộng sự hỗ trợ của khái niệm *subroutines* từ **structured programming**, đồng thời kế thừa các khái niệm như *scope* / *control flows* để mở rộng thế giới của **programming language**, giúp việc viết một chương trình đơn giản hơn. Procedural language sẽ xoay quanh các khái niệm như `record`, `module`,`procedure`, `procedure call`. Thuở sơ khai thì **procedural programming** hỗ trợ cho phép các procedure thực hiện các thao tác thực tiếp lên vùng nhớ, giá trị của các thanh ghi / biến (`record`), đồng thời cũng hỗ trợ việc gom nhóm procedure liên quan tới nhau thành nhóm - `module` để dễ dàng quản lý, sử dụng ở nhiều nơi. Khi `procedure call` được gọi thì `instruction pointer` sẽ lập tức di chuyển đến nơi khai báo và thực hiện việc thao tác dựa trên dữ liệu được gọi (thường là địa chỉ của giá trị để thao tác trực tiếp). Sau khi `procedural call` kết thúc thì giá trị sẽ được cập nhật ở vị trí cũ và `instruction pointer` quay lại nơi được gọi và tiếp tục xử lý các `instruction` khác. Điều cần nói ở đây là **procedural programming** cần phải có sự hỗ trợ từ **structured language**. `procedural` có thể hiểu tương tự như `function` (hàm). Tuy nhiên hàm thì thay vì cập nhật trực tiếp giá trị ở ô nhớ thì lại trả về giá trị mới để chúng ta có thể tính toán bước tiếp theo mà không cần phải cập nhật giá trị ở ô nhớ cũ (thường là lưu lại để chuẩn bị tính toán tiếp). Sự khác biệt giữa `procedural` & `function` đa phần đến từ cách truyền giá trị vào và trả về giá trị. 

Một ngôn ngữ lập trình không nhất thiết chỉ hỗ trợ một **paradigm**, mà có thể nhiều **paradigm**. Một ví dụ điển hình hiện tại là phần lớn các ngôn như lập trình bậc cao đều hỗ trợ **structured** / **procedural language** (câu lệnh điều khiển và function/procedure). Ví dụ về **pass by value** & **pass by reference** là 2 trường hợp để phân biệt rõ nhất về sự khác nhau giữa **function/procedure** (Nếu không muốn thì cũng không sao cả vì sự khác biệt rất nhỏ). Để phân biệt rõ hơn về 2 khái niệm này thì cần phải tìm hiểu về các thanh ghi `callee ($s)` & `caller ($t)`, tuy nhiên việc này cũng ít cần thiết nốt, vì đa phần các ngôn ngữ lập trình đã làm thay ta công việc này rồi. Hãy xem xét 2 ví dụ của **C++**sau đây.

```cxx
#include <iostream>

int mean(int a,int b){
    return (a+b)/2;
}

void swap(int *a, int *b){
    int t = *a;
    *a = *b;
    *b = t;
}

int main(){
  int a = 100;
  int b = 21;
  cout << mean(a,b) << "\n";
  swap(&a,&b);
  cout << a <<" "<< b;
}
```

# Objet Oriented Programming & Functional Programming
**Functional Programming** (lập trình hướng chức năng) là một loại phong cách lập trình, mục đích chủ yếu xoay quanh về việc các `function` (chức năng) được hoàn thành như thế nào. Chúng ta chỉ cần đưa vào input vào một chức năng thì sẽ có ngay lập tức output hợp lệ. **Functional Programming** thường xoay quanh việc áp dụng, tạo ra các function như thế nào. Những function này thường là một dãy các expression (biểu thức) để mapping (ánh xạ, biến đổi, et cetera) dữ liệu đầu vào thành dữ liệu đầu ra (input & output) mà tránh việc dữ liệu bị thay đổi (mutable state), side effects khiến cho code trở trên dễ hiểu, debug, test, et cetera. Javascript có hỗ trợ **Functional Programming**, tuy nhiên nên tránh nhầm lẫn giữa việc hỗ trợ **Functional Programming** và thuần **Functional Programming** (purely **functional programming** - được kế thừa dựa trên lambda calculus). **Functional Programming** xem function là *first-class citizen*, lưu ý rằng ở đây không mang ý nghĩa phân biệt thượng đẳng/hạ đẳng mà là nhằm mục đích để chỉ rằng tư tưởng của **Functional Programming** xoay quanh hàm - tức là function sẽ được *fully supported*. **Functional Programming** là một khái niệm rất mới, dần tiếp cận với các lập trình viên từ các framework của Javascript (Hook của React), nhưng những ngôn ngữ **pure functional programming language**  thì lại khá là kén (haskell, lisp, et cetera). Sau đây sẽ là một vài ví dụ về **Functional Programming** ở trong Javascript.

```javascript
const array = [5, 19, 16, 7, 5, 10, 17, 5, 2, 17, 15, 15, 17, 8, 15, 14, 8, 1, 11, 17]
const array_less_than_15 = array.filter((element)=> element < 15)
console.log(array_less_than_15)
```

```javascript
const array = [5, 19, 16, 7, 5, 10, 17, 5, 2, 17, 15, 15, 17, 8, 15, 14, 8, 1, 11, 17]
const array_less_than_15 = []
for(let i = 0;i < array.length ; i++){
    if (array[i]<15){
        array_less_than_15.push(array[i])
    }
}
```

Một điều lưu ý ở đây là chúng ta vẫn sử dụng method built-in của `Array` (filter) (vẫn có dính dáng tới OOP, vì Javascript hỗ trợ cả 2 paradigm này). Ngoại trừ **Functional Programming** thì chúng ta còn có OOP, nói về sự phổ biến của OOP thì không cần phải bàn cãi, vì hiện tại đây là một tượng đài không thể được vượt qua tại thời điểm hiện tại. Giống như **Functional Programming** luôn luôn xoay quanh function thì OOP lại đặt `class` & `object` là *first-class citizen* và mọi khái niệm xung quanh. Ưu thế của OOP nằm ở việc mô hình hoá mọi khái niệm ở trong chương trình trở thành những thứ quen thuộc, xung quanh đời sống khiến mọi chuyện trở nên dễ dàng tiếp cận với những người mới. Điểm khác biệt lớn nhất so với **Functional Programming** có lẽ là state - trạng thái - cũng có thể hiểu là dữ liệu. **Functional Programming** dành phần lớn thời gian để giúp chúng ta mapping - ánh xạ - từ input thành ouput thông qua các function. OOP thì lại quan tâm tới state và cách thay đổi state một cách internally (nội bộ). Có 4 đặc tính cơ bản mà OOP cung cấp cho chúng ta đó là : **Abstraction**, **Encapsulation**, **Inheritance**, and **Polymorphism**. Ngoại trừ 4 *principles* (nguyên lý) cơ bản này ra thì còn có nhiều **Design Pattern**. **SOLID guidelines** là một bộ gồm 5 nguyên tắc cơ bản để thiết kế một chương trình dựa trên OOP. Không dám bàn sâu về vì còn non và xanh. Hãy cùng xem xét ví dụ để hiểu rõ hơn (ít nhất là tổng quan). Điều thú vị của Javascript là có thể cài đặt thêm prototype/method rất nhanh dựa trên **Prototype-based implementation**.

```javascript
const array = [5, 19, 16, 7, 5, 10, 17, 5, 2, 17, 15, 15, 17, 8, 15, 14, 8, 1, 11, 17]
// thay bằng arrow function sẽ không chạy nhé
Array.prototype.less_than = function(number){
    let array = new Array();
    if (!number){
        throw new Error(`Expected a number, but got ${typeof number}`)
    }
    for(let element of this){
        if (element<number){
            array.push(element)
        }
    }
    return array
}
let array_less_than_15 = array.less_than(15)
console.log(array_less_than_15)
```

# Imperative / Declarative Programming
**Imperative** là phong cách lập trình mà chúng ta phải khai báo từng bước thực hiện và tính toán ở mỗi dòng code, mỗi bước cực kỳ quan trọng vì nó nó thể ảnh hưởng tới kết quả. Đơn giản hơn, chúng ta phải cung cấp **công thức** giúp biến đổi *input* thành *output*.

**Declarative** thì ít rắc rối hơn, chúng ta chỉ cần khai báo input và sử dụng các công thức có sẵn một cách phù hợp để tạo ra output, chúng ta có thể thêm một vài tuỳ chọn vào, nhưng hầu hết đều không ảnh hưởng tới công thức. Bằng cách này, chúng ta tiết kiệm rất nhiều thời gian và công sức khi viết code, không cần phải mất thời gian chỉ rõ rằng phải làm gì ở bước này, bước kia, lặp như nào, điều kiện ra sao,et cetera.

Điều khác biệt ở 2 programming style này nằm ở thứ tự. Bạn là một người pha chế rất giỏi, biết rất nhiều công thức pha cà phê ngon, và bây giờ bạn đang chỉ cho cái máy làm từng bước để đạt được kết quả như bạn. Kiến thức cốt lõi ở đây là **công thức** - cách giải quyết vấn đề - khi nói về **Imperative**, điều quan trọng nhất là **HOW**. Còn đối với **Declarative** thì **WHAT** hoặc là **WHICH** mới là thứ quan trọng. Giả sử chúng ta có một cái máy pha coffee có thể pha mọi loại coffee trên đời với nhiều công thức có sẵn. Vậy thứ chúng ta cung cấp chỉ đơn giản là hạt coffee và chọn thứ coffee chúng ta muốn. Điều quan trọng ở đây, là chúng ta cần phải biết được các công thức có sẵn **làm việc gì** và vận dụng nó ra sao. 

Điển hình về sự khác nhau thì ta có thể xem lại 2 ví dụ trên.

```javascript
const array = [5, 19, 16, 7, 5, 10, 17, 5, 2, 17, 15, 15, 17, 8, 15, 14, 8, 1, 11, 17]
const array_less_than_15 = []
for(let i = 0;i < array.length ; i++){
    if (array[i]<15){
        array_less_than_15.push(array[i])
    }
}
console.log(array_less_than_15)
```


```javascript
const array = [5, 19, 16, 7, 5, 10, 17, 5, 2, 17, 15, 15, 17, 8, 15, 14, 8, 1, 11, 17]
const array_less_than_15 = array.filter((element)=> element < 15)
console.log(array_less_than_15)
```

---
# References & more resources
- https://qz.com/852770/theres-a-limit-to-how-small-we-can-make-transistors-but-the-solution-is-photonic-chips/
- https://en.wikipedia.org/wiki/Computer
- https://www.cs.uaf.edu/courses/cs301/2014-fall/notes/goto/
- https://en.wikipedia.org/wiki/Procedural_programming
- https://www.educative.io/edpresso/pass-by-value-vs-pass-by-reference
- https://stackoverflow.com/questions/373419/whats-the-difference-between-passing-by-reference-vs-passing-by-value
- https://en.wikipedia.org/wiki/Functional_programming
- https://en.wikipedia.org/wiki/Object-oriented_programming


### P/S:
Nếu có gì sai sót xin gửi email cho mình để cập nhật, xin cảm ơn!

