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


