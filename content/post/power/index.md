---
title: "Power, root, logarithms"
description: "Power, exponent, root, logarithm and relevant things"
date: 2021-05-23T19:18:38+07:00
draft: false
math: true
slug: "power"
categories:
    - Math
    - Programming Language
tags:
    - Math
image: cover.png

---
Một trong nhiều vấn đề khá là nan giải (thực ra không phải là nan giải, "người ta" đã giải quyết nó từ lâu rồi - từ có nghĩa là cách tiếp cận khó khăn) trong lập trình, hoặc toán học đó là phép toán luỹ thừa. Một câu hỏi có thể hay được đặt ra đó là: "Làm sao để tính luỹ thừa bậc n của một số bất kỳ?". Vấn đề trở nên rất đơn giản nếu như chúng ta sử dụng các ngôn ngữ lập trình Javascript, Python, hoặc là các thư viện kèm theo của các ngôn ngữ bậc thấp như "math.h" của C / \<cmath\> của C++. Nhưng trong trường hợp không không thể sử dụng các built-in, chúng ta tính luỹ thừa như thế nào?

# Exponent as natural number
Bằng một vài định nghĩa toán học cơ bản, ta biết được rằng phép toán luỹ thừa là việc thực hiện các phép nhân liên tục. Cụ thể hơn, *base* được nhân với chính bản thân *n* lần.

$$
 \underbrace{b^n = b.b.b...b}_\text{n times} 
$$

Bằng định nghĩa này thì ta có thể tự implement như sau
```javascript
function pow(base,exp){
    let p = 1;
    for(let i=0;i<exp;i++){
        p = p*base
    }
    return p;
}
```

Tuy nhiên chỉ có bấy nhiêu đây thì vẫn chưa đủ, ta cần phải cover cả các trường hợp đặc biệt như là `NaN,0,1,infinity`. Ta cũng có thể dựa trên các định nghĩa trên để cải tiến hàm `pow` tốt hơn.

```javascript
function pow(base,exp){
    if (base == 1) return 1;
    if (base == 0) return 0;
    if (exp == 0) return 1;
    if (exp == 1) return base;
    if (isNaN(base) || isNaN(exp)) return NaN;
    if (isFinite(base) || isFinite(exp)) return Infinity;

    let p = 1;
    for(let i=0;i<exp;i++){
        p = p*base
    }
    return p;
}
```
Như vậy thì chúng ta đã có thể tự implement một hàm luỹ thừa manually mà không dựa vào thư viện. Tuy vậy, thực sự thì hàm luỹ thừa này vẫn còn thiếu sót rất nhiều, cụ thể là **Nếu số mũ của chúng ta số thực thì sao?** Đến đây thì đoạn code ở trên lại không thể giúp chúng ta. **Euler** sẽ giúp chúng ta vấn đề này.

# Logarithms
Cái gì cũng có mặt trái của nó, (chỉ có bản mặt của tôi là không có người yêu), chúng ta thường có những phép toán trái nghịch nhau như (công >< trừ, nhân>< chia, hàm >< nghịch hàm,...). Điều này cũng đúng với phép luỹ

Vì lười nên tác giả chưa viết tiếp
magical number
euler's number 
irrational constant
natural log

365 ?


Trước khi nói về **e** thì chúng ta cần phải biết về **compound interest** (lãi kép). 
---
# References & more resources
- https://www.netlib.org/fdlibm/e_pow.c
- https://www.youtube.com/watch?v=AuA2EAgAegE
- https://www.youtube.com/watch?v=_-x90wGBD8U
- https://stackoverflow.com/questions/9799041/efficient-implementation-of-natural-logarithm-ln-and-exponentiation/63773160#63773160

