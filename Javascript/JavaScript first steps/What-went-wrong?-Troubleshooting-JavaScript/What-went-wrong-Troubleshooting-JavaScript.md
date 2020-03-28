# What went wrong? Troubleshooting JavaScript
- Điều tiên quyết: 
    Trình độ máy tính cơ bản, hiểu được HTML và CSS, JS là gì
- Mục tiêu: 
    Để có được khả năng và sự tự tin để bắt đầu sửa chữa các vấn đề trong mã của riêng bạn.

## Types of error
    Có 2 kiểu lỗi thường xuất hiện: 
        `Systax errors` - Lỗi cú pháp
        `Logic errors`  - Lỗi logic
    
## Fixing syntax errors
1. Để biết lỗi xuất hiện từ đâu, bạn sẽ phải mở 
    - Chuột phải -> `inspect`.
    - Hoặc Ctrl + Shift + C hoặc phím F12.
    Bạn sẽ nhìn thấy thông báo lỗi ở bên dưới nếu trong code của bạn xảy ra lỗi.
2. Thành phần của lỗi bao gồm:
    1. 1 dấu đỏ `x` được biểu thị là lỗi.
    2. 1 thông báo lỗi hiển thị lỗi.
    ```js
        TypeError: guessSubmit.addeventListener is not a function
    ```
    3. `Learn more` một liên kết đến MDN trang để giải thích lỗi vừa thông báo.
    4. Tên của tệp JavaScript, liên kết đến tab Trình gỡ lỗi của các công cụ dành cho nhà phát triển. Nếu bạn theo liên kết này, bạn sẽ thấy dòng chính xác nơi lỗi được tô sáng.
    5. Liệt kê lỗi xuất phát ở đâu, cụ thể là `dòng nào : ký tự nào`.

