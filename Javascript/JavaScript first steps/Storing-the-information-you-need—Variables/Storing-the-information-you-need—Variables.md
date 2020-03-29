# Storing the information you need — Variables
Mục tiêu: Để làm quen với những điều cơ bản của các biến JavaScript.

## Tools you need
Trình duyệt hỗ trợ JS tốt nhất: Chrome, Firefox, Opera, Safari... chuyển sang tab console để test code.
## What is a variable?
1 biến chứa 1 giá trị như số mà chúng ta sử dụng nó trong 1 tổng, hoặc 1 chuỗi trong 1 câu. Điều đặc biệt của biến đó là nó có thể thay đổi giá trị trong nó.
```html
<button>Press me</button>
```
```js
const button = document.querySelector('button');

button.onclick = function() {
  let name = prompt('What is your name?');
  alert('Hello ' + name + ', nice to see you!');
}
```
> NOTE: Biến chứa 1 hoặc nhiều giá trị, bạn có thể ví chúng như những thùng cotton nhỏ lưu chữ đồ đạc.

## Declaring a variable
Để sử dụng biến, đầu tiên bạn phải khai báo nó. có 2 kiểu biến bạn sẽ sử dụng nhiều nhất là `let` và `var` được theo dõi bởi tên bạn muốn theo dõi.
```js
let myName = 'Cong';
var myAge = 26;
```

## Updating a variable
Khi một biến đã được khởi tạo với một giá trị, bạn có thể thay đổi (hoặc cập nhật) giá trị đó bằng cách chỉ cần cung cấp cho nó một giá trị khác. Hãy thử nhập các dòng sau vào bảng điều khiển của bạn:
```js
myName = 'Bob';
myAge = 40;
```

[Bạn có thể theo dõi nó ở đây](https://github.com/Iamcong/Kanban-Board/blob/learning/Javascript/JavaScript%20first%20steps/A-first-splash-into-JavaScript/A-first-splash-into-JavaScript.md).