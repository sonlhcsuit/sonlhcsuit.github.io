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

Chúng ta có thể khái quát lịch sử máy tính bằng bài viết khác, nhưng sau thời gian dài phát triển, thì công dụng chủ yếu của máy tính là để tính toán dựa trên input và sinh ra output. Máy tính ở thời điểm ban đầu có kích thước rất to ( bằng cả căn phòng), theo thời gian chuyển dời thì kích thước ngày càng giảm dần bởi vì CPU (Central Processing Unit) - lõi của máy tính càng ngày càng nhỏ dựa vào công nghệ nano. Thời điểm ban đầu, CPU được chế tạo dựa trên bóng đèn dây tóc - biểu thị trạng thái bật (số 0) và tắt (số 1). Công nghệ phát triển giúp chúng ta thay thế bóng đèn bằng bóng bán dẫn nhỏ hơn bóng đèn cả nghìn lần. Nhờ vào việc thay đổi sử dụng transistor (bóng bán dẫn) vào việc chế tạo CPU khiến cho kích thước CPU càng ngày càng nhỏ (đồng thời dẫn tới kích thước máy tính ngày càng nhỏ dần). Có một định luật gọi là Moore phát biểu rằng, cứ sau một chu kỳ thời gian nhất định thì số lượng transistor trên một đơn vị diện tích ( $cm^2$ ) sẽ tăng gấp đôi. Công nghệ nano còn có nhiều không gian để phát triển, chu kỳ của Moore's Law là 2 năm (Đến thời gian hiện tại thì mình không dám chắc vì không biết rõ là công nghệ nano có thể đạt tới kích thước bao nhiêu. Theo thông tin tham khảo thì 1 transistor đạt kích thước 0.2 nanometer - $10^{-9}$ meter). Bởi vì lí do chỉ có thể sử dụng 2 trạng thái on/off (cho dòng điện chạy qua) của một bóng đèn / transistor nên máy tính chỉ hiểu được số nhị phân. Kết hợp các transistor và các mạch logic khiến cho CPU có thể thực hiện việc tính toán. Và computer được gọi là bởi computer bởi vì được sinh ra với mục đích là **compute**.

![Block Diagram of Computer](image-1.png)

CPU của máy tính được dựa trên những thành phần cơ bản gồm ALU (Arithmetic & Logic Unit - Bộ xử lý tính toán), Main Memory (Bộ nhớ chính), CU (Control Unit - Bộ điều khiển) và các thành phần khác như cache, register, et cetera. Chúng ta khiến computer thực hiện tác vụ bằng việc sử dụng instructions set ( bộ lệnh) phù hợp đã được định nghĩa sẵn bởi mỗi nhà thiết kế. Mỗi máy tính có một đặc điểm khác nhau như việc thiết kế kiến trúc, thiết kế các ALU khác nhau (cùng 1 việc thực hiện phép toán + nhưng có nhiều cách) nên instructions set cũng khác nhau nốt. Các developer/scientist thực hiện công việc xây dựng các chương trình hằng ngày bằng việc sử dụng instructions set bằng mã nhị phân. Điểm yếu của phương pháp này là chương trình viết trên một máy tính sẽ không chạy trên máy tính khác kiến trúc.

Các instructions set này còn được gọi là **machine language/binary language**, đây là loại ngôn ngữ lập trình sơ khai nhất. Programming language (ngôn ngữ lập trình) được tạo ra bởi con người, được sử dụng nhằm mục đích giao tiếp với máy tính, khiến cho máy tính thực hiện các hành vi do người dùng (developer/scientist) chỉ định.

# Classification of Programming Language

Có rất nhiều cách để phân loại ngôn ngữ lập trình dựa trên nhiều tiêu chí. Một tiêu chí hay dùng nhất là dựa trên độ khó của việc viết, và một vài tiêu chí khác: **low-level** & **high-level**, hai loại ngôn ngữ này có các đặc điểm sau:
- low-level:
    - machine langugage
    - assembly language
- high-level:
    - structural language
    - procedural language
    - object oriented language
    - functional language

Ưu điểm của ngôn ngữ low-level rất rõ ràng: siêu nhanh, chạy trực tiếp trên CPU. Tuy nhiên yếu điểm cũng không kém cạnh: chỉ gồm bit 0 hoặ 1 (machine code) dẫn tới khó đọc, khó đọc, khó viết, dể ẩn tàng lỗi, khó bảo trì. Một điểm phát triển của assembly code so với machine code là có thể sử dụng english word (dễ nhớ) cải thiện code đáng kể. Tuy nhiên vẫn rất để lập trình, và đặc biệt là không có cấu trúc rõ ràng, chỉ gồm một list instructions. Yêu cầu cần assembler để phiên dịch assembler code thành machine code. Tuy nhiên vẫn cần assembler khác nhau dành cho mỗi máy tính

Ưu của của ngôn ngữ high-level thì không cần ai phải bàn cãi: viết code một cần, có thể chạy ở hầu hết loại máy tính. Câu lệnh tiếng anh rất dễ đọc và dễ viết, cung cấp khả năng trừu tượng. Yếu điểm là phải cần một compiler/interpreter khác nhau cho mỗi loại máy tính. Điều cần phải củng cố compiler/interpreter cho từng loại kiến trúc (x86,et cetera). Ưu điểm rất là rõ ràng, và ai cũng sử dụng high-level language nên việc phân loại tiếp theo sẽ tập trung vào các high-level language. Lưu ý việc phân loại ở đây, không phải là phân loại từng ngôn ngữ lập trình mà là phân loại các paradigm (mô hình ngôn ngữ lập trình).

# Structured Programming & Procedural Programming
Structured Programming nghĩa là lập trình có cấu trúc, vậy thế nào là có cấu trúc? "Cấu trúc" ở đây nói về việc xử lý các dòng code một cách hợp lý bằng việc hỗ trợ thêm các khái niệm như: blocks/scopes, control flows (condition & repitition), subroutines. Tại sao lại hỗ trợ thêm các khái niệm này? Trước khi các khái niệm này sinh ra thì đa phần các chương trình đều viết bằng assembly nên việc sử dụng câu lệnh jump/goto là cực kỳ phổ biến. Hãy xem xét ví dụ về việc rẽ nhánh và lặp sau đây.

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

Nhìn vào 2 ví dụ trên thì mọi chuyện không khác biệt, nếu bạn đã cố gắng hiểu những dòng comment. Tuy nhiên, khi debug assembly code thì thực sự là một cực hình (ít nhất thì mình có từng chạy code assembly khi học Computer Architecture - Kiến trúc máy tính), đặc biệt là phải soi rất kỹ lệnh `cmp` và lệnh `jump` các loại, đồng thời còn quan sát từng label nữa. Việc sử dụng câu lệnh goto sẽ khiến cho code chúng ta được tối ưu (không gian dòng lệnh, chức năng, tốc độ, et cetera) nhưng lại mang đến một hậu quả kinh khủng là cực hình khi debug (nhìn nhầm 1 dòng là không biết instructions pointer chạy đi đâu luôn). Để giải quyết vấn đề này thì một vài khái niệm đã xuất hiện giúp cho cuộc sống của các lập trình viên dễ dàng hơn bằng việc hỗ trợ thêm khái niệm scopes / control flows giúp code dễ đọc hơn khi phải thực hiện các thao tác như so sánh, lặp, hàm, et cetera. Hỗ trợ thêm nhiều từ khoá giúp con người dễ dàng làm quen hơn.

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

Bàn về procedural programming, cơ bản là mở rộng sự hỗ trợ của khái niệm subroutines từ structured programming, đồng thời kế thừa các khái niệm như scope / control flows để mở rộng thế giới của programming language, giúp việc viết một chương trình đơn giản hơn. Procedural language sẽ xoay quanh các khái niệm như `record`, `module`,`procedure`, `procedure call`. Thuở sơ khai thì procedural programming hỗ trợ cho phép các procedure thực hiện các thao tác thực tiếp lên vùng nhớ, giá trị của các thanh ghi / biến (`record`), đồng thời cũng hỗ trợ việc gom nhóm procedure liên quan tới nhau thành nhóm - `module` để dễ dàng quản lý, sử dụng ở nhiều nơi. Khi `procedure call` được gọi thì instruction pointer sẽ lập tức di chuyển đến nơi khai báo và thực hiện việc thao tác dựa trên dữ liệu được gọi (thường là địa chỉ của giá trị để thao tác trực tiếp). Sau khi `procedural call` kết thúc thì giá trị sẽ được cập nhật ở vị trí cũ và instruction pointer quay lại nơi được gọi và tiếp tục xử lý các instruction khác. Điều cần nói ở đây là procedural programming cần phải có sự hỗ trợ từ structured language. `procedural` có thể hiểu tương tự như `function` (hàm). Tuy nhiên hàm thì thay vì cập nhật trực tiếp giá trị ở ô nhớ thì lại trả về giá trị mới để chúng ta có thể tính toán bước tiếp theo mà không cần phải cập nhật giá trị ở ô nhớ cũ (thường là lưu lại để chuẩn bị tính toán tiếp). Sự khác biệt giữa procedural & function đa phần đến từ cách truyền giá trị vào và trả về giá trị. 

Một ngôn ngữ lập trình không nhất thiết chỉ hỗ trợ một paradigm, mà có thể nhiều paradigm. Một ví dụ điển hình hiện tại là phần lớn các ngôn như lập trình bậc cao đều hỗ trợ structured / procedural language (câu lệnh điều khiển và function/procedure). Ví dụ về pass by value & pass by reference là 2 trường hợp để phân biệt rõ nhất về sự khác nhau giữa function/procedure (Nếu không muốn thì cũng không sao cả vì sự khác biệt rất nhỏ). Hãy xem xét 2 ví dụ của C++ sau đây.

```cxx
```
# Objet Oriented Programming & Functional Programming


# Prototype ? How Javascript implement OOP 

# pass

# this & relevants concepta

# Better Method

---
# References & more resources
- https://qz.com/852770/theres-a-limit-to-how-small-we-can-make-transistors-but-the-solution-is-photonic-chips/
- https://en.wikipedia.org/wiki/Computer
- https://www.youtube.com/watch?v=Pn5znSOGHcs
- https://www.cs.uaf.edu/courses/cs301/2014-fall/notes/goto/
- https://en.wikipedia.org/wiki/Procedural_programming
- https://www.educative.io/edpresso/pass-by-value-vs-pass-by-reference
- https://www.youtube.com/watch?v=aYjGXzktatA
- https://www.youtube.com/watch?v=A38y7OO8OK4