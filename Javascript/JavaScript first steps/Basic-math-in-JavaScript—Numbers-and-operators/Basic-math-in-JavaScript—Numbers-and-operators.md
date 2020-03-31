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
Là những toán tử gán giá trị cho biến. Toán tử đơn giản nhất là `=`, rất nhiều lần. hiểu đơn giản là nó sẽ gán giá trị bên phải cho biến bên bên trái.
```js
var x = 3; // x giữ giá trị 3
var y = 4; // y giữ giá trị 4
x = y; // x giờ giữ giá trị giống hệt với y, 4
```
Tôi sẽ giới thiệu cho bạn 4 toán tử gán thông dụng nhất: `+=`, `-=`, `*=`, `/=` tương ứng như:
    - `+=`: `x = x + 1`
    - `-=`: `x = x - 1`
    - `*=`: `x = x * 1`
    - `/=`: `x = x / 1`
## Học chủ động: định cỡ của hộp canvas
```js
let x = 50; let y = 50;

// Edit the two lines below here ONLY
x = 50;
y = 50;

ctx.fillStyle = 'green';
ctx.fillRect(10, 10, x, y);
```
Hãy chủ động copy đoạn code trên và chỉnh sửa giá trị được chỉ định x, y để xem thay đổi và cách vận hành của nó, không cần quan tâm đến các chức năng hay thuật toán nhé. Ý tôi nói là phép gán :)

## Toán tử so sánh
Để trả về kết quả kiểu `bool (true / false)`.
`===` : bằng tuyệt đối        -  Kiểm tra xem liệu hai giá trị trái phải có giống hệt nhau hay không. vd: `5 === '5' // result: false`
`!==` : không bằng tuyệt đối  -  Kiểm tra xem liệu hai giá trị trái phải không giống hệt nhau hay không. vd: `5 !== '5' // result: true`
`<`   : nhỏ hơn               -  Kiểm tra xem giá trị bên trái có nhỏ hơn giá trị bên phải hay không. vd: `5 < 6 // result: true`
`>`   : lớn hơn               -  Kiểm tra xem giá trị bên trái có lơn hơn giá trị bên phải hay không. vd: `6 > 5 // result: true`
`<=`  : nhỏ hơn hoặc bằng     -  Kiểm tra xem giá trị bên trái có nhỏ hơn hoặc bằng giá trị bên phải hay không. vd: `3 <= 2 // result: false`
`>=`  : lớn hơn hoặc bằng     -  Kiểm tra xem giá trị bên trái có lớn hơn hoặc bằng giá trị bên phải hay không. vd: `5 >= 4 // result: true`

> Đôi khi chúng ta sẽ thấy một số trường hợp sẽ sử dụng `==` và `!=`, toán tử này sẽ kiểm tra sự giống nhau về giá trị nhưng không kiểm tra sự giống nhau về kiểu dữ liệu.

```js
3 == '3' // true
3 === '3' // false
```

Toán tử so sánh rất hữu ích và chúng được sử dụng rất rộng rãi trong chương trình của bạn, như:
    + Hiển thị nhãn ký tự chính xác tuỳ thuộc liệu một chức năng nào đó đang bật hay tắt
    + Hiển thị hộp thoại trò chơi kết thúc khi một trò chơi kết thúc hoặc hộp thoại chiến thắng khi đạt được chiến thắng trong trò chơi
    + Hiển thị câu chào mừng hợp với dịp lễ/ hội nào đó
    + Phóng to / thu nhỏ bản đồ tuỳ theo nút nào được nhấn

```html
<button>Start machine</button>
<p>The machine is stopped.</p>
```
```js
var btn = document.querySelector('button');
var txt = document.querySelector('p');

btn.addEventListener('click', updateBtn);

// Toggle
function updateBtn() {
  if (btn.textContent === 'Start machine') {
    btn.textContent = 'Stop machine';
    txt.textContent = 'The machine has started!';
  } else {
    btn.textContent = 'Start machine';
    txt.textContent = 'The machine is stopped.';
  }
}
// Tạo file .html rồi thử nó để thấy nó.
```


