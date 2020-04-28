# Useful string methods - Các phương thức String hữu ích

Bài này, chúng ta sẽ học được những điều cơ bản liên quan đến chuỗi, như tìm độ dài, nối, tách chuỗi, thay thế ký tự trong 1 chuỗi cho 1 chuỗi khác và hơn thế nữa.

## Finding the length of a string - Độ dài của chuỗi.
Sử dụng thuộc tính `length` để lấy độ dài : 
```js
let str = 'hello world';
console.log(str.length); // 11
```
Kết quả trả về sẽ là 11, vì có 11 ký tự bao gồm cả dấu cách `space`. Điều này thật hữu ích bởi nhiều lý do: như validation với field phone-number, kiếm tra độ dài ...

## Retrieving a specific string character - Lấy 1 ký tự chuỗi cụ thể
Bạn có thể lấy bất kì một ký tự bên trong 1 chuỗi với cặp ngoặc vuông `[]`. Bên trong dấu ngoặc vuông bạn có thể là 1 số hoặc một biến bất kì như vd bên dưới:
```js
let str = 'hello';
console.log(str[0]); // h
```
> Hãy nhớ, máy tính luôn đếm từ 0, `không phải 1`.<br/>
- Bạn cũng có thể lấy kí tự cuối cùng như sau: 
```js
let str = 'hello world';
lastLetter = str.length - 1;
console.log(lastLetter); // d
```
Vì máy tính luôn lấy từ 0 mà muốn lấy kí tự cuối cùng thì phải n-1.

## Finding a substring inside a string and extracting it - Tìm chuối con bên trong 1 chuỗi và trích xuất nó.
1. Đôi khi bạn muốn tìm từ khóa bên trong 1 văn bản lớn, bạn có thể thực hiện bằng hàm `indexOf()`, lấy 1 tham số duy nhất - chuỗi bạn muốn tìm kiếm.
```js
let str = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Dapibus ultrices in iaculis nunc sed augue lacus. Quam nulla porttitor massa id neque aliquam';
let keyWord = str.indexOf('Quam nulla');
console.log(keyWord); // 174
console.log(str.indexOf('hello')); // -1
```
> NOTE: Như trên đã đề cập đến nó sẽ luôn tính từ 0, 1, 2 ... khi tìm từ khóa nếu nó tồn tại trong đoạn text cần tìm nó sẽ trỏ đến vị trí tìm thấy từ khóa đó.
Nếu không tìm thấy kết quả sẽ trả về `-1`.

2. Khi bạn biết vị trí từ khóa mà bạn muốn lấy và ký tự cuối cùng trong 1 chuỗi. `slice()` dùng để trích xuất nó:
```js
// old string : 
let browserType = 'Mozilla';
browserType.slice(0,3);
// Output: Moz
```
`slice(start, end)` có 2 tham số: 
    1. start: vị trí bắt đầu trích xuất.
    2. end: vị trí kết thúc, kết quả sẽ không bao gồm phần tử  cuối cùng.

> Note: Nếu bạn muốn lấy toàn bộ chỉ sau một ký tự nào đó có trong chuỗi thì bạn có thể dùng 1 tham số. Tham số thứ 2 là không bắt buộc.
`slice(start)`.
```js
// old string : 
let browserType = 'Mozilla';
browserType.slice(2);
// Output: zilla
```
## Changing case - Thay đổi trường hợp.
Phương thức dùng cho chuỗi: `toLowerCase()` and `toUpperCase()` đưa chuỗi và chuyển tất cả chúng đến dạng chữ thường hoặc chữ in hoa (lower- or uppercase). Điều này có thể hữu ích, ví dụ nếu bạn muốn bình thường hóa tất cả dữ liệu do người dùng nhập trước khi lưu trữ vào cơ sở dữ liệu

```js
let radData = 'My NaMe Is MuD';
radData.toLowerCase(); // Output: my name is mud
radData.toUpperCase(); // Output: MY NAME IS MUD
```
## Updating parts of a string - Cập nhật các phần của chuỗi.
Có thể thay thế 1 subString bên trong 1 string sử dụng: `replace()`. Nó có 2 tham số:
> `replace(searchvalue, newvalue)` <br/>
> searchvalue: từ khóa cần tìm. <br/>
> newValue: từ khóa cần thay thế.
```js
let dataString = 'mozilla';
dataString.replace('mozill', 'coron'); // Output: corona
```
> Nếu bạn muốn thay thế tất cả những từ có trong văn bản, bạn có thể làm như sau:
```js
let str = 'hello all member, hello student and hello everybody';
str.replace(/hello/g, 'hi');
// Output: hi all member, hi student and hi everybody
```




