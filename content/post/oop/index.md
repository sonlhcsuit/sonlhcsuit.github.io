---
title: "Javascript and OOP"
description: "Object Oriented Programming in Javascript & relevant concepts"
date: 2021-05-04T08:21:25+07:00
draft: false
math: true
slug: "oop-js"
categories:
    - programming-language
    - javascript
    
image: cover.png

---

# History about Programming Languages & Computer

Chúng ta có thể khái quát lịch sử máy tính bằng bài viết khác, nhưng sau thời gian dài phát triển, thì công dụng chủ yếu của máy tính là để tính toán dựa trên input và sinh ra output. Máy tính ở thời điểm ban đầu có kích thước rất to ( bằng cả căn phòng), theo thời gian chuyển dời thì kích thước ngày càng giảm dần bởi vì CPU (Central Processing Unit) - lõi của máy tính càng ngày càng nhỏ dựa vào công nghệ nano. Thời điểm ban đầu, CPU được chế tạo dựa trên bóng đèn dây tóc - biểu thị trạng thái bật (số 0) và tắt (số 1). Công nghệ phát triển giúp chúng ta thay thế bóng đèn bằng bóng bán dẫn nhỏ hơn bóng đèn cả nghìn lần. Nhờ vào việc thay đổi sử dụng transistor (bóng bán dẫn) vào việc chế tạo CPU khiến cho kích thước CPU càng ngày càng nhỏ (đồng thời dẫn tới kích thước máy tính ngày càng nhỏ dần). Có một định luật gọi là Moore phát biểu rằng, cứ sau một chu kỳ thời gian nhất định thì số lượng transistor trên một đơn vị diện tích ( $cm^2$ ) sẽ tăng gấp đôi. Công nghệ nano còn có nhiều không gian để phát triển, chu kỳ của Moore's Law là 2 năm (Đến thời gian hiện tại thì mình không dám chắc vì không biết rõ là công nghệ nano có thể đạt tới kích thước bao nhiêu. Theo thông tin tham khảo thì 1 transistor đạt kích thước 0.2 nanometer - $10^{-9}$ meter). Bởi vì lí do chỉ có thể sử dụng 2 trạng thái on/off (cho dòng điện chạy qua) của một bóng đèn / transistor nên máy tính chỉ hiểu được số nhị phân. Kết hợp các transistor và các mạch logic khiến cho CPU có thể thực hiện việc tính toán. Và computer được gọi là bởi computer bởi vì được sinh ra với mục đích là **compute**.

![Block Diagram of Computer](image-1.png)

CPU của máy tính được dựa trên những thành phần cơ bản gồm ALU (Arithmetic & Logic Unit - Bộ xử lý tính toán), Main Memory (Bộ nhớ chính), CU (Control Unit - Bộ điều khiển) và các thành phần khác như cache, register, et cetera. Chúng ta khiến computer thực hiện tác vụ bằng việc sử dụng instructions set ( bộ lệnh) phù hợp đã được định nghĩa sẵn bởi mỗi nhà thiết kế. Mỗi máy tính có một đặc điểm khác nhau như việc thiết kế kiến trúc, thiết kế các ALU khác nhau (cùng 1 việc thực hiện phép toán + nhưng có nhiều cách) nên instructions set cũng khác nhau nốt. Các developer/scientist thực hiện công việc xây dựng các chương trình hằng ngày bằng việc sử dụng instructions set bằng mã nhị phân. Điểm yếu của phương pháp này là chương trình viết trên một máy tính sẽ không chạy trên máy tính khác kiến trúc.

Các instructions set này còn được gọi là **machine language/binary language**, đây là loại ngôn ngữ lập trình sơ khai nhất.

# Classification




low level & high leve
run direct on CPU
Có rất nhiều phong cách lập trình tồn tại từ xưa đến tận bây giờ. Đại khái có 4 phong cách lập trình gồm
- Structured Programming
- Procedural Programming
- Objet Oriented Programming
- Functional Programming

# Object Oriented Programming

# Prototype ? How Javascript implement OOP 

# this & relevants concepta

# Better Method

---
# References & more resources
- https://qz.com/852770/theres-a-limit-to-how-small-we-can-make-transistors-but-the-solution-is-photonic-chips/
- https://en.wikipedia.org/wiki/Computer
- https://www.youtube.com/watch?v=Pn5znSOGHcs
- https://www.youtube.com/watch?v=aYjGXzktatA
- https://www.youtube.com/watch?v=A38y7OO8OK4