# Basic math in JavaScript — numbers and operators
Mục tiêu: Để làm quen với những điều cơ bản của toán học trong JavaScript.

## Everybody loves math

1. Types of numbers
Có nhiều thuật ngữ khác nhau để mô tả các kiểu số thập phân khác nhau, chẳng hạn:
- Integers là số nguyên, ví dụ 10, 400, or -5.
- Floating point numbers (số thực dấu phẩy động) có dấu chấm thập phân và vị trí thập phân, ví dụ 12.5, và 56.7786543.
- Doubles là một kiểu số thực dấu phẩy động đặc biệt có độ chính xác cao hơn số thực dấu phẩy động bình thường (độ chính xác liên quan đến số lượng vị trí sau dấu chấm thập phân).

Chúng tôi còn có một số kiểu hệ số khác! Thập phần là hệ cơ số 10 (tức là sử dụng 0–9 trong từng hàng từ đơn vị đến chục trăm...), nhưng chúng tôi cũng có những thứ như là:

- Binary — Cấp độ thấp nhất trong ngôn ngữ máy; 0 và 1.
- Octal — Cơ số 8, dùng 0–7 trong từng hàng.
- Hexadecimal — Cơ số 16, dùng 0–9 và tới a–f trong từng hàng. Có lẽ bạn từng sử dụng kiểu số này khi thiết lập màu sắc trong CSS.

> Tin mừng thứ hai là không giống như một số ngôn ngữ lập trình khác, JavaScript chỉ có duy nhất một kiểu dữ liệu cho số, đó là, Number. Điều này nghĩa là dù bạn gặp phải kiểu số học nào trong JavaScript, bạn cũng có thể xử lý chúng cùng một cách.

2. Với tôi tất cả chỉ là số
**Mở trong 1 cửa sổ mới**

2.1. Bật Console lên và khai báo biến:
```js
    var myInt = 5;
    var myFloat = 6.667;
    myInt;
    myFloat;
```
2.2. Giá trị số học không cần tới cặp dấu nháy — thử khai báo và khởi tạo thêm vài cặp biến nữa trước khi chuyển sang bước tiếp theo.
> Kiểm tra xem hai biến vừa tạo của chúng ta có cùng kiểu dữ liệu không, sử dụng `typeof`.
```js
typeof myInt;
typeof myFloat;
```
## Toán tử số học
Toán tử số học là những toán tử căn bản để ta dùng cho phép tính:

|Toán tử         |Tên            |Mục đích                     |Ví dụ            |
|----------------|---------------|-----------------------------|-----------------|
|+               |`Cộng`         |Cộng hai số lại với nhau.    | 6 + 9           |
|-               |`Trừ`          |Trừ số  bị trừ.              | 20 - 15         |
|*               |`Nhân`         |Tích của 2 số                | 3 * 7           |  
|/               |`Chia`         |Số bị chia.                  | 10 / 5          |
|%               |`Chia lấy dư`  |Trả về phần dư               | 8 % 3 = 2       |

## Thứ tự ưu tiên toán tử
- Nhân và chia luôn được thực hiện trước, rồi tới cộng và trừ (phép tính luôn thực hiện từ trái qua phải)
- Nếu bạn muốn vượt thứ tự ưu tiên toán tử, bạn có thể đặt cặp ngoặc tròn quanh phần mà bạn muốn thực hiện trước. Thế nên để trả về giá trị 6, ta sẽ làm như sau:
```js
(num2 + num1) / (8 + 2);
```
## Toán tử tăng và giảm
Đôi khi bạn sẽ muốn cộng hoặc trừ liên tục thêm/ bớt một với một biến số học nhất định. Việc này có thể dễ dàng thực hiện bằng toán tử tăng (++) và toán tử giảm (--).
> NOTE: <br/>
Bạn chỉ có thể sử dụng toán tử này cho 1 biến và không thể dùng trực tiếp bằng số như `5--` hoặc `3++`. Điều này sẽ sai.

```js
// Biểu thức đúng:
let i=3; i++ // tương đương: i = i + 1;
let a = 5; a-- // tương đương: a = a -1;
```
> Phân biệt cách dùng ++i và i++ và --i và i--
```js
// ++i (--i) sẽ tăng (giảm) giá trị của i, và sau đó trả về giá trị tăng(giảm).
i = 1;
j = ++i;
(i is 2, j is 2)

//i++ (i--) sẽ tăng(giảm) giá trị của i, nhưng trả về giá trị ban đầu iđược giữ trước khi tăng(giảm).
i = 1;
j = i++;
(i is 2, j is 1)
```
## Toán tử gán

