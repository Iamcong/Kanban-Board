# JavaScript — Dynamic client-side scripting
> JavaScript - kịch bản phía máy khách động
> Javascript là ngôn ngữ cho phép bạn thực hiện những công việc phức tạp trên website. Nó có thể hiển thị cập nhật nội dung kịp thời, bản đồ tương tác, hoạt ảnh 2D / 3D đồ họa hoặc cuộn các hộp video...

**JavaScript** là một ngôn ngữ dễ học và bắt buộc khi bạn muốn phát triển web hoặc app. Nó liên quan mật thiết đến 2 ngôn ngữ **HTML** và **CSS**, trước khi tìm hiểu và học **JS**, bạn phải học trước về 2 ngôn ngữ này.

## Js cho phép bạn thực hiện một vài điều như:

- Lưu trữ giá trị vào các biến (variables).
- Thao tác trên các đoạn văn bản (String).
- Chạy code phản hồi lại những sự kiện đang xảy ra ở trên website.
- Và nhiều hơn thế nữa.
> Tuy nhiên thứ mà thậm chí còn thú vị hơn nữa là các lớp tính năng (functionality) được xây dựng trên lõi của ngôn ngữ JavaScript. Cái được gọi là **Giao Diện Lập Trình Ứng Dụng** (Application Programming Interfaces-APIs) trao thêm cho bạn siêu sức mạnh để sử dụng trong code JavaScript.

## APIs

Hiểu nôm na là các bộ code được xây dựng sẵn cho phép nhà phát triển triển khai và thực hiện trên những gì nó có. APIs tạo cho bạn đầy đủ những dữ liệu và bạn có thể lắp ghép vào ứng dụng, công việc của bạn một cách hoàn hảo.

**APIs được chia thành 2 loại :** **Browser APIs** và **Third party APIs**

## Browser APIs (APIs Trình Duyệt)
> Được tích hợp sẵn trong trình duyệt web, có khả năng phơi bày dữ liệu từ môi trường máy tính xung quanh hoặc làm những điều phức tạp hữu ích.

1. **DOM** (*Document Object Models*) **APIs** cho phép bạn :
- Điều khiển HTML và CSS, loại bỏ và thay đổi HMTL.
- Áp dụng style mới vào một trang một cách linh hoạt.
2. **Geolocation API** tiếp nhận thông tin địa lí. 
> Đây là cách `Google Maps` tìm ra vị trí của tôi trên bản đồ.
3. **Canvas** và **WebGL** APIs cho phép bạn tạo hoạt cảnh đồ họa 2D, 3D.
4. **Audio và Video APIs** như `HTMLMediaElement` và `WebRTC` cho phép bạn làm việc với đa phương tiện (MultiMedia). như chạy video, audio. và video ngay trong trang web hoặc thu video từ cam và hiển thị trên máy tính người khác.

>**Note**: Một số **trình duyệt cũ** hơn sẽ **không hỗ trợ** đầy đủ cho ngôn ngữ **JavaScript**. Vì vậy bạn nên sử dụng một số trình duyệt hiện đại như : Chrome, Firefox, Opera..
## Third party APIs (bên thứ 3)
> Điều này sẽ không phải mặc định của trình duyệt. Phải lấy mã code hoặc thông tin người dùng từ đâu đó trên web. Ví dụ :
- `Twitter APIs` cho phép hiện thị những `Tweets` mới nhất trên trang web của bạn.
- `Google Maps APIs` và `OpenStreetMaps API` cho phép bạn nhúng bản đồ trong website. và rất nhiều chức năng khác.

> **Note: ** APIs là  nâng cao, và nó sẽ không bao gồm những module này. Bạn có thể tìm thấy những điều này về APIs: [Client-side web APIs module](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs).

## What is JavaScript doing on your page?
> Javascript đang làm gì trên web ?
 ### Tóm tắt : 
- Khi 1 trang web được tải trong trình duyệt, code HTML, CSS, JS sẽ được load bên trong 1 tab (môi trường thực hiện ). Điều này như là nhà máy sẽ cung cấp cho bạn nguyên vật liệu (the codes), output là sản phẩm (trang web).

- JS được thực thi bởi công cụ JS của trình duyệt, được chạy sau HTML, CSS được thông dịch và đặt bên trong 1 trang web. Điều này đảm bảo cấu trúc và kiểu của 1 trang đã được đặt đúng lúc JavaScript bắt đầu chạy.

## Browser security
- Mỗi 1 tab là một không gian riêng để chạy code (được gọi là "môi trường thực thi" theo thuật ngữ kỹ thuật) - nghĩa là trong hầu hết các trường hợp, mã của 1 tab là chạy riêng biệt, Hoặc mã trong 1 tab không thể ảnh hưởng đến tab khác hoặc trang web khác ở tab khác .
## Javascript running order
> Khi trình duyệt gặp 1 khối JS, nó sẽ chạy tuần tự từ đầu đến cuối. 
```js
const para = document.querySelector('p');

para.addEventListener('click', updateName);

function updateName() {
  let name = prompt('Enter a new name');
  para.textContent = 'Player 1: ' + name;
}
```
Trình tự :
1. Đầu tiên nó sẽ chạy dòng 1 và đính kèm 1 sự kiện nghe ngóng ở dòng 3 khi thẻ p được click thì hàm updateName() sẽ được chạy. (Kiểu tái sử dụng của một khối trong JS được gọi là function). Hỏi tên người dùng mới, sau đó, nó sẽ tự update tên và hiển thị.
2. Ngược lại, nếu ta thay đổi `para.addEventListener('click', updateName);` trước dòng 1 thì sẽ có lỗi xảy ra. vì biến para là chưa được định nghĩa.
## Interpreted versus compiled code
> Js là ngôn ngữ rất nhẹ.

## Server-side versus client-side code
> Server-side vs Client-side
- Trong bối cảnh lập trình web. Client-side code là chạy trên máy tính người dùng, khi 1 trang web được xin thấy. JS được tải, chạy và hiển thị trên trình duyệt
- Mặt khác, mã được chạy trên máy chủ thì kết quả đã được tải và hiển thị trên trình duyệt Ta thấy một số Server-side được chạy bởi 1 vài ngôn ngữ phổ biến như : PHP, Python, Ruby... và JS (Sử dụng node.js).
- Bạn có thể tìm hiểu về Server-side chạy bằng node.js tại đây : [Dynamic Websites – Server-side programming](https://developer.mozilla.org/en-US/docs/Learn/Server-side).
## Dynamic versus Static code
> Javascript được thêm trong HTML giống như cách thức thêm CSS. Trong khi CSS nhận \<link\> || \<style\> thì Script chỉ nhận \<Script\>
* Có 2 cách để thêm JS vào trong HTML:
    1. Lồng code vào trong cặp thẻ \<script\>\</script\>
    ```html
    <script>

        // JavaScript goes here

    </script>
    ```
    2. Thêm bằng liên kết src:
    ```html
    <script src="script.js" defer></script>
    ```

* Chúng ta có thể thêm JS ở bất cứ nơi nào trong HTML, và thường xuất hiện khi sử lý sự kiện:
    
    Trong thẻ HTML
    ```html
        <button onclick="createParagraph()">Click me!</button>
    ```
## Script loading strategies
> Chiến lược tải tập lệnh

- Có một số vấn đề liên quan đến tải các lệnh trong JS. Dường như nó ko hề đơn giản. Có một vấn đề chung thường xảy ra trong tất cả các trang HTML trong tiến trình xuất hiện.
- Nếu đang sử dụng JavaScript để thao tác các phần tử trên trang (hoặc chính xác hơn là [Document Object Model](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Manipulating_documents#The_document_object_model) - DOM), code sẽ không chạy được vì tiến trình của JS sẽ chạy trước HTML.
- Trong ví dụ trước ta thấy các mã Script chỉ được bao bọc bởi thẻ \<Script\>. Điều này có thể làm đoạn mã JS đó sẽ chạy không như chúng ta mong đợi.
- Để đảm bảo điều trên ko xảy ra và trong hầu hết các đoạn mã code trong JS chúng ta sẽ thấy:
```js
document.addEventListener("DOMContentLoaded", function() {
  ...
});
```
> Điều này có nghĩa là: <br/>
> Khi nội dung được tải xong **(DOMContentLoaded)** thì mới thêm các sự kiện **(addEventListener)** trong vòng bao.

> Trong đó:<br/>
> addEventListener: nghe ngóng sự kiện.<br/>
> DOMContentLoaded: nội dung được tải xong.<br/>

> Chú ý:<br/>
> Trong một số trường hợp bên ngoài (sử dụng src) chúng ta sẽ cần đến **defer - sự hoãn lại** 
> Tuy nhiên, chúng ta sẽ không dùng defer cho giải pháp nội bộ, vì defer chỉ trong cho các tập lệnh bên ngoài.


>**WARNING**: Một số trường hợp sẽ để trước thẻ đóng \</body\>. Tuy nhiên nó sẽ thường gây ra các vấn đề về code hoặc hiệu suất tải trang.

## async(đồng bộ) and defer(trì hoãn)
> Có 2 giải pháp cho khối lệnh JS tránh xảy ra lỗi.
1. async
> async script sẽ tải các khối script mà không rendering trang và sẽ thực thi nó ngay sau khi script được tải xuống. không có sự đảm bảo nào cho tập lệnh sẽ chạy theo bất kỳ thứ tự nào. Chỉ có điều chúng sẽ ngăn phần còn lại của trang hiển thị. 

> Sử dụng async tốt nhất khi các tập lệnh chạy độc lập với nhau và không phụ thuộc vào nhau.

> ví dụ:
```js
<script async src="js/vendor/jquery.js"></script>

<script async src="js/script2.js"></script>

<script async src="js/script3.js"></script>
```
Ở ví dụ này bạn sẽ không thể dựa vào thứ tự các khối js sẽ được tải. jquery.js cũng có thể được tải trước hoặc sau 2 tệp còn lại và trong trường hợp này, jquery sẽ có thể bị lỗi vì `jquery` sẽ không được định nghĩa tại thời điểm JS chạy.

2. defer
> Sẽ chạy script theo thứ tự xuất hiện trong trang và thực thi chúng ngay sau khi script và nội dung được tải.

```html
<script defer src="js/vendor/jquery.js"></script>

<script defer src="js/script2.js"></script>

<script defer src="js/script3.js"></script>
```
Tất cả script với thuộc tính defer sẽ được tải theo thứ tự xuất hiện trong trang. Vì vậy, trong ví dụ 2 các file sẽ được tải tuần tự từ trên xuống dưới.

### `Tổng kết:`
  - Nếu code của bạn không cần chờ phân tích cú pháp (parsing) và có thể chạy độc lập(independently) mà không phụ thuộc (dependencies) thì sử dụng async.
  - Ngược lại, nếu code của bạn cần phải chờ xử lý và phụ thuộc vào các đoạn mã script khác tải chúng sử dụng defer và đặt tương ứng của họ \<script\> theo thứ tự bạn muốn thực thi chúng.

## Comment
Cũng như HTML, CSS. Js cũng có cách viết comment code để trình duyệt chấp nhận nó. Nó đơn giản, giới thiệu ý nghĩa cho đoạn mã của bạn (nếu sau một thời gian quay trở lại code thì bạn sẽ vẫn hiểu nó). Comments là rất tuyệt vời, và sẽ sử dụng thường xuyên.
- Có 2 cách comments:
  1. Trên một dòng
  ```js
    // Iam a comment
  ```
  2. Trên nhiều dòng:
  ```js
    /*
      I am also
      a comment
    */
  ```
- Ví dụ dễ hiểu:
```js
// Function: creates a new paragraph and appends it to the bottom of the HTML body.

function createParagraph() {
  let para = document.createElement('p');
  para.textContent = 'You clicked the button!';
  document.body.appendChild(para);
}
```