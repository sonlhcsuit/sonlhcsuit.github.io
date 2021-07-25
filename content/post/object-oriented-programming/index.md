---
title: "Object Oriented Programing Implementation"
description: "No Description"
date: 2021-05-23T20:34:57+07:00
draft: false
math: false
slug: "object-oriented-programming"
categories:
    - Javascript
    - Python
image: cover.jpg

---
# Disadvantages of previous paradigms
Các phương pháp lập trình trước kia (procedural programming & structured programming) đòi hỏi một sự quản lý cực kỳ chặt chẽ khi code. Tuy nhiên với bản chất của procedural programming là viết nhiều dòng lệnh chạy từ trên xuống thì thực sự có quản lý có tốt tới đâu thì chúng ta vẫn gặp trường hợp bad code khi chương trình trở trên to hơn (nhiều tính năng hơn). Một bước tiến quan trọng đó chính là định nghĩa `function`/`procedure`/`module` (nhiều functions liên quan tới nhau được đặt trong cùng 1 file) được tạo ra giúp cho việc code nên dễ dàng hơn (tái sử dụng code). Tuy nhiên từ một ví dụ thực tế (1 trận đấu pokemon chẳng hạn), nhiều hàm đều có quyền truy cập tới các giá trị global để thay đổi dữ liệu( ví dụ máu, mp, pp, ...). Từ một góc độ nào đó, việc này vẫn còn tồn đọng nhiều rủi ro chưa xuất hiện. Bằng việc thay đổi khái niệm của một chương trình `Algorithms + Data Structure = Programs` thành những một công thức tổng quảt quát hơn đã giúp sinh ra lập trình hướng đối tượng.

# Object Oriented Programming 
Dựa vào công thức: `Algorithms + Data Structure = Programs`, ta có hiểu đơn giản: `Data Structure` ở đây là dữ liệu (chính xác hơn thì là cấu trúc dữ liệu) và `Algorithms` là hàm (chính xác hơn là giải thuật). Các thành phần trên góp phần tạo nên chương trình, tuy nhiên lại khó để quản lý khi mà chương trình càng ngày càng lớn, càng khó để mô hình hoá, để quản lý hơn. Từ góc độ này, chúng ta có `Data` ở một nơi và `Function` ở một nơi,  thì nảy sinh ra ý tưởng: "Tại sao không gom data & function lại thành 1 nhỉ?" Ý tưởng cơ bản của OOP nằm ở việc gom nhiều `data` và `function` liên quan tới nhau (nghĩa là thực hiện việc thay đổi trên `data`) chung với nhau thành một đơn vị gọi là `object`. Và việc mô hình hoá cũng dễ dàng hơn khi chúng ta liên tưởng các `object` tới những thứ cụ thể ở cuộc sống thực tế.

`Object` gồm những thành phần sau:
- `Attribute`: nhằm thể hiện thông tin, dữ liệu của `object`
- `Behavior`: nhằm thể hiện các hành động mà `object` có thể thực hiện

Để dễ hình dung thì hãy tưởng tượng một con `mèo anh lông ngắn` là một thì `attribute` (còn được gọi là `characteristics`) sẽ là những thông tin liên quan tới bản chất của `object` (lông màu xám, lông ngắn, mắt xanh, đuôi cụt, 3 tuổi, nặng 10kg, ...). Về phần `behavior` là những hành động liên quan tới đối tượng (ăn: giúp cơ thể phát triển, cân nặng tăng,...)

# Class & Object
`Object` & `Class` là 2 khái niệm cơ bản, nền tảng, quan trọng nhất của OOP. 

`Object` gồm `attribute` & `behavior` (`inner function`,`method`,`member function`, ...). Các `object` sẽ tương tác với nhau thông qua các `method` (`inner function`), và cập nhật lại dữ liệu của `object` gián tiếp, không phải trực tiếp bằng cách gán giá trị mới cho các `attribute` mà thông qua con đường là sự dụng các hàm chức năng (`method`). Đây là đặc điểm cơ sở của tính chất đầu tiên của OOP : `Data encapsulation & information hidding`

`Class` là một khái niệm trừu tượng hơn, bao quát hơn `object`, là khuôn mẫu để định hình các `object` (các `object` có `attribute` nào và `behavior` nào) từ dưới góc độ thực tế. Hãy xem xét thử một vài game RPG có các `class` character như là `knight`, `warrior`, `magician`,... Tuỳ thuộc vào các `class` này, ta có thể biết được khả năng của nhân vật `knight` thì có máu nhiều và phòng thủ cao, `magician` thì có sát thương lớn và phòng thủ kém,... Từ góc độ lập trình, thì `object` được xem là thành phần của `class`. Lấy một ví dụ thực tế, ta có 1234 là số nguyên, thuộc về tập hợp số nguyên, và bởi vì nhiều ngôn ngữ đã được cài đặt sẵn số nguyên là gì, nên chúng ta có thể sử dụng ngay lập tức mà không cần phải khai báo thêm, tất nhiên là đi kèm các behavior khác như cộng trừ nhân chia các số khác. `Class` có xu hướng tổng quát, còn `object` thì có xu hướng cụ thể. Đơn giản hơn thì `Class` chính là khuôn mẫu của `object`, chúng ta từ một `class`, có thể tạo ra nhiều `object` thuộc `class` đó. Và những `object` thuộc cùng `class` với nhau, sẽ có các `behavior`, `attribute` như nhau (tất nhiên là khác giá trị) đã được định nghĩa chung ở `class`, `object` là `instance` của `class` (thể hiện của `class`).

Khi viết một chương trình theo dạng OOP, chúng ta dành đa phần thời gian vào việc khai báo class , sau đó tạo các object và để chúng tương tác với nhau (cộng phân số, nông trại vui vẻ,...)

# 4 fundamental principles of OOP
Lập trình hướng đối tượng là tư tưởng, là phong cách lập trình, hơn là một kỹ thuật. Bản chất của hướng đối tượng có thể dựa trên các nguyên lý cơ bản sau:
- Data encapsulation : Các đối tượng chỉ có thể tương tác với nhau thông qua các method phù hợp, không được trực tiếp thay đổi attribute của nhau. `Attribute` là dữ liệu sẽ được bảo vệ, che giấu ở trong đối tượng đó.
- Inheritance: Các class có thể có nhiều attribute giống nhau, khi khai báo class thì ta không cần phải khai báo lại mà có thể tận dụng các attribute & method có sẵn để tận dụng thời gian và không gian thông qua việc kế thừa. Các derived class (class con) sẽ kế thừa sản nghiệp (attribute & method) của base class (class cha). Mục đích chính của kế thừa là để nhiều object có chung nhiều đặc điểm để dễ bề quản lý.
- Polymerization: Nhiều derived class có một cách thực hiện các behavior được kế thừa từ base khác nhau. Ví dụ như hành động ăn thì con bò sẽ khác sư tử (vẫn là nạp năng lượng vào cơ thể - thay đổi các attribute), di chuyển thì con cá sẽ bơi bằng mang và ngựa thì chạy bằng chân. Tuỳ thuộc vào từng class cụ thể mà sẽ có nhiều cách thể hiện cùng một behavior đã được kế thừa từ base class. 
- Abstraction : Abstraction thông thường đi kèm với Polymerization để tạo nên một cặp bài trùng hoàn hảo. Abstraction mang tính khái quát hoát, cố gắng tìm điểm chung nhất để có thể tạo nên class chung nhất, rồi sau đó kết hợp với polymerization để tạo ra sự đa dạng trong cách thực hiện nhưng lại dẫn tới cùng kết quả. Nói ví dụ về điện thoại, ta có rất nhiều điện thoại ở trên đời, nhưng ta có cần phải quan tâm hết cơ chế chúng không (Ví dụ làm sao để gọi điện, nhắn tin, tính toán,..). Nếu với một người làm việc với kỹ năng cứng là chế tạo điện thoại thì cần, nhưng với end-user thì có cần thiết không? End-user không cần biết điện thoại được chế tạo như nào (gồm CPU gì, RAM bao nhiêu, Cache thế nào, làm sao màn hình cảm ứng lại xài được, ...) mà chỉ quan tâm tới việc xài như thế nào. Việc gửi tin nhắn hoặc gọi điện 1 Nokia cũng có thể gửi được tin nhắn cho 1 cái iPhone XXX Pro Max. Abstraction ở đây chính ta việc trừu tượng hoá các behavior chung nhất (gửi tin nhắn, gọi điện,...) và kết hợp với polymerization để tạo nên sự đa dạng nhưng vẫn dễ dàng quản lý.

**Ở trên chỉ là đôi chút kinh nghiệm nhỏ, tâm đắc được rút ra từ bản thân tác giả.**
# Implement language with OO supported
Có 2 cách để implement một ngôn ngữ hỗ trợ hướng đối tượng (OO supported). Đó là class-base & prototype-base.
Class-base là cách implement (cài đặt) ngôn ngữ lập trình hướng đối tượng chặt chẽ nhất, thể hiện được khía cạnh mạnh mẽ của OO (hướng đối tượng), các ngôn ngữ bậc trung như C++, Java, C#,... được cài đặt theo cách này. Tuy nhiên điểm yếu là khi bắt đầu code với các ngôn ngữ này thì nên tảng về hướng đối tượng cực kỳ quan trọng, kỹ thuật lập trình là thứ không thể thiếu, đôi khi cài đặt dài dòng rườm ra mất thời gian của coder nhưng đánh đổi được là dễ quản lý, dễ tìm lỗi và bảo trì. Nôm na là sẽ đánh đổi công sức của coder lấy về một source code tốt (hoặc ít nhất thì đó là lý tưởng). Cách ngược lại thì giúp coder viết code nhanh và mượt hơn, không strict chặt chẽ, dễ tiếp cận với người mới  


# How Javascript implements OOP

# How Python implements OOp

---
# References & more resources

### P/S:
Nếu có gì sai sót xin gửi email cho mình để cập nhật, xin cảm ơn!
