# Handling text — Strings in JavaScript
Trong lập trình chuỗi là một phần nhỏ của văn bản. Trong bài viết này chúng ta sẽ cùng tìm hiểu tất cả các đặc điểm chúng mà bạn cần phải biết về chuỗi khi học JavaScript, như là tạo chuỗi, escaping quotes trong chuỗi và kết hợp chuỗi lại với nhau.

## Creating a string
1. Để bắt đầu nó, chúng ta theo dõi đoạn code dưới đây:
```js
var string = 'The revolution will not be televised.';
string;
```
Tương tự như phép gán cho số học. Chúng ta khai báo 1 biến, khởi tạo nó vói kiểu dữ liệu `String`, và returning giá trị đó. Chỉ khác nhau ở đây là khi bạn viết 1 chuỗi, bạn cần có dấu `'` hoặc `"` được bao quanh giá trị.
2. Làm ơn đừng làm điều này, nó sẽ xảy ra lỗi nếu như bạn viết những dòng code như sau:
```js
var badString = This is a test;
var badString = 'This is a test;
var badString = This is a test';
var badString = 'This is a test";
```
3. Thử khai báo kiểu cho biến:
```js
var badString = string;
badString;
```
badString đã được thiết lập kiểu dữ liệu là `string`.

4. Single quotes vs. double quotes - `'` vs `"`
    1. Bạn có thể sử dụng 2 kiểu dấu  `'` hoặc `"`, chúng sẽ làm việc.
        ```js
        var sgl = 'Single quotes.';
        var dbl = "Double quotes";
        sgl;
        dbl;
        ```
    2. Không được viết đoạn code theo kiểu dưới đây, chúng sẽ gây ra lỗi cho bạn.
    ```js
    var badQuotes = 'What on earth?";
    ```
    3. Trình duyệt sẽ hiểu đúng khi 2 dấu nháy đã được bao quanh giá trị.
    ```js
    var sglDbl = 'Would you eat a "fish supper"?';
    var dblSgl = "I'm feeling blue.";
    sglDbl;
    dblSgl;
    ```
    4. Trong một vài trường hợp bạn sẽ không thể sử dụng dấu nháy trong dấu nháy như sau:
    ```js
    var bigmouth = 'I've got no right to take my place...';
    ```
## Escaping characters in a string - Thoát các ký tự trong chuỗi
Để fix lỗi về những dấu nháy mà bạn muốn nó hiển thị trong những đoạn text (không phải trong code) của bạn thì bằng cách đặt dấu gạch chéo `\` ngay trước ký tự.
```js
var bigmouth = 'I\'ve got no right to take my place...';
bigmouth;
```

## Concatenating strings - chuỗi kết nối
1. Kết nối chuỗi như việc cộng một number với number nhớ toán tử `+`. 
    ```js
    var one = 'Hello, ';
    var two = 'how are you?';
    var joined = one + two;
    joined;
    // Ouput: 'Hello, how are you?'
    ```
2. Bạn có thể sử dụng một hoặc kết nối nhiều chuỗi với nhau.
    ```js
    let one ="one ", two = "two ";
    var multiple = one + one + one + one + two;
    multiple;
    // Output: "one one one one two "
    ```
## Concatenation in context - Kết nối các ngữ cảnh (something...)
```html
<button>Press me</button>
```
```js
var button = document.querySelector('button');

button.onclick = function() {
  var name = prompt('What is your name?');
  alert('Hello ' + name + ', nice to see you!'); 
}
```
Biến name chính là context và điều này nó sẽ kết nối với chuỗi.

## Numbers vs. strings
1. Điều gì sẽ xảy ra khi bạn cộng chuỗi vs số ?
```js
'Front ' + 242; // Output: "Front 242"
```
2. Bạn có thể cộng 2 số như cộng 2 chuối nếu bạn để chúng trong dấu nháy.
```js
'1' + '2'; // Output: "12"
```
3. Nếu bạn có 1 `biến`  kiểu `Number` bạn muốn chuyển (convert) đến 1 `string` và ngược lại làm như sau:
- `Number` sẽ convert bất kỳ điều gì được thông qua trong 1 số. Nếu nó có thể:
    ```js
    var myString = '123';
    var myNum = Number(myString);
    typeof myNum;
    ```
- Mặt khác, Nếu bạn muốn chuyển đổi số thành chuỗi, hãy sử dụng toString():
    ```js
    var myNum = 123;
    var myString = myNum.toString();
    typeof myString;
    ```
> Mặc định: nếu bạn nhập 1 số hay giá trị bất kỳ trong thẻ input thì nó sẽ luôn là 1 string. vì vậy,nếu bạn cần phải đưa nó về kiểu số thì bạn sẽ dùng `Number()`

