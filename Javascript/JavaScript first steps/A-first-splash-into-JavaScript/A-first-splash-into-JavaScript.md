# A first splash into JavaScript
> Lần đầu làm chuyện ấy

Trong khóa học này, ta sẽ học các lý thuyết và đan sen thực hành. "Bước các bước".

> Prerequisites (điều kiện tiên quyết): <br>
    - Kiến thức cơ bản: về máy tính, HTML, CSS và hiểu được JS là gì!<br/>
Objective (Mục tiêu): <br/>
    - Có chút kinh nghiệm, biết viết JS cơ bản, và hiểu được viết để làm gì! 

```js
let randomNumber = Math.floor(Math.random() * 100) + 1;
const guesses = document.querySelector('.guesses');
const lastResult = document.querySelector('.lastResult');
const lowOrHi = document.querySelector('.lowOrHi');

const guessSubmit = document.querySelector('.guessSubmit');
const guessField = document.querySelector('.guessField');

let guestCount = 1, resetButton;
```

1. Biến và hằng (variables and constants) dùng để  chứa dữ liệu mà chương trình sẽ sử dụng.
2. Variables cơ bản để chứa giá trị như: số, text, mảng, đối tượng...
3. Tạo ra biến sử dụng keyword: **let** hoặc **var**. [Sự khác biệt giữ let vs var](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Variables#The_difference_between_var_and_let)).
4. **Const** dùng để lưu giá trị không bao giờ thay đổi (cố định, không thay đổi được).

Quy tắc đặt tên biến:
1. Tên biến không chứa ký tự đặc biệt.
2. Không sử dụng dấu gạch dưới `"_"` để bắt đầu đặt tên biến. Dấu gạch dưới chỉ nên sử dụng trong `constructs JS`, nên điều này dễ nhầm lẫn.
3. Không sử dụng số  bắt đầu đặt tên biến.
```js
    // false
    let 9a, 3xxx;

    // True
    let a, b, x1,x2, X1, X2;
```
4. Quy ước đặt tên biến [lower camel case](https://en.wikipedia.org/wiki/CamelCase#Variations_and_synonyms), Sử dụng hoa thường cho ký tự đầu tiên, sau đó viết hoa ký tự đầu tiên cho từ tiếp theo. vd: `nameVariables`
5. Đặt tên biến gắn với ý nghĩa của nó. Không đặt tên biến quá dài, hoặc khó hiểu.
```js
    let isDisplay = true;
    let isActived = false;
    let listStudents = [];
    let person = {};
```
6. Phân biệt chữ thường và in hoa.

Cuối cùng: Tránh đặt tên biến với các từ khóa, các hàm có sẵn trong JS như: `function, this, let, var, for ... `và điều này sẽ gây ra lỗi.

### Variable types: 
> JavaScript sẽ tự động hiểu biến đó là kiểu dữ liệu gì. Nếu biến chứa cặp `".."` hoặc `'...'` thì nó sẽ hiểu là string.
1. Numbers 
```js
let myAge = 17;
let floatVariable = 2.03;
```
2. Strings
```js
let myText = 'Hello JavaScript!';
let myName = "Iam Cong";
```
3. Booleans
> Có 2 giá trị: `true` và `false`.
```js
let iAmAlive = true;
let test = 6 < 3; // output: false
```
4. Arrays
> Mảng là một đối tượng duy nhất chứa nhiều giá trị được đặt trong dấu ngoặc vuông và được phân tách bằng dấu phẩy.
```js
let myNameArray = ['Chris', 'Bob', 'Jim'];
let myNumberArray = [10, 15, 40];
```
> Mảng sẽ tính các key (chỉ số - index) từ 0 trở đi. 

Như mảng `myNameArray` có 3 giá trị tương ứng chỉ số là `0-1-2`.
```js
myNameArray[0]; // should return 'Chris'
myNumberArray[2]; // should return 40
```
5. Objects
> Là kiểu có chứa nhiều thông tin về đối tượng đó. <br>vd: persion bao gồm: name, phone, height, weight, language they speak...
```js
let person = { 
    name : 'Phantom', 
    phone: '0100120101', 
    height: '1.52', 
    weight: '100', 
    languages: [
        {language: 'Tieng Viet'},
        {language: 'Tieng anh'}
    ];
```
## Dynamic typing
> JavaScript là 1 ngôn ngữ động, nghĩa là nó sẽ tự động hiểu kiểu của biến mà ko cần phải định nghĩa trước.

```js 
let myString='hello world' 
```
> Ngay cả khi giá trị chứa số, nó vẫn là một chuỗi, vì vậy hãy cẩn thận:
```js
let myNumber = '500'; // oops, this is still a string
typeof myNumber;
myNumber = 500; // much better — now this is a number
typeof myNumber;
```

# Functions
```js
function checkGuess() {
  alert('I am a placeholder');
}
```
> Functions là khối lệnh được tái sử dụng nhiều lần, sử dụng những đoạn code giống nhau.
- Cú pháp: 
```js
function functionName() {
    // code here...
}
``` 
# Operators - Toán tử
Các toán tử JavaScript cho phép chúng tôi thực hiện các bài kiểm tra, làm toán, nối các chuỗi với nhau và những thứ khác.
- Các Toán tử:
    === : 2 vế phải hoàn toàn giống nhau
    !== : 2 vế là khác nhau
    <   : nhỏ hơn
    >   : lớn hơn

# Conditionals - Điều kiện
Giá trị trả về của điều kiện là kiểu `Bool` chỉ có đúng (true) hoặc sai (false).
```js
let a = 1, b = -1;
a > b;              // output true
true === false;     // output false
6 === '6';          // output false
6 == '6';           // output true
``` 
# Events - Sự kiện
- Sự kiện là điều gì đó sẽ xảy ra khi người dùng hoặc trình duyệt tác động vào như click, cuộn chuôt, load trang, thay đổi tab, tắt tab, tải lại trang, xem video ...
- Các cấu trúc đang lắng nghe sự kiện được gọi là `event listeners`. Và các function được gọi trong sự kiện thì được gọi là `event handlers` (xử lý sự kiện).
```js
guessSubmit.addEventListener('click', checkGuess);
```
Trong đó: 
    guessSubmit : nơi lắng nghe sự kiện.
    addEventListener: sự kiện xảy ra khi `click`.
    checkGuess: tên function.

# Loops - Vòng lặp
Cú pháp:

```js
for (let i = 1 ; i < 21 ; i++) { 
    console.log(i)
}
// output 1 2 3 ... 20
```
Điều này cho phép đoạn code trên sẽ console log trên trình duyệt 20 lần

[xem thêm tại đây](https://developer.mozilla.org/vi/docs/Learn/JavaScript/First_steps/A_first_splash).

