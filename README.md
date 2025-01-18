# Câu hỏi phỏng vấn

### Hỏi về HTML

1. **Virtual DOM là gì? Tại sao quan trọng?**
   - Là một bản sao nhẹ của DOM thật, được lưu trong bộ nhớ
   - **Hiệu suất cao:** So sánh và chỉ cập nhật phần thay đổi lên DOM thật.
   - **Trải nghiệm tốt:** Giảm thao tác trực tiếp với DOM thật, tránh làm chậm ứng dụng.

2. **Tác dụng của doctype?**
   - Khai báo kiểu tài liệu HTML để trình duyệt biết cách render
   - Đảm bảo trang web được hiển thị ở chế độ standards mode

3. **Điều gì cần chú ý khi xây dựng và phát triển các trang web đa ngôn ngữ?**
   - Sử dụng thẻ `lang` và `charset` phù hợp
   - Hỗ trợ RTL (Right-to-Left) cho một số ngôn ngữ
   - Tổ chức content theo cấu trúc i18n

4. **Thuộc tính `data-` dùng để làm gì?**
   - Lưu trữ dữ liệu tùy chỉnh trong HTML
   - Truy cập dữ liệu thông qua JavaScript Dataset API

5. **Khác nhau giữa cookie, sessionStorage và localStorage?**
   - **Cookie:** 4KB, gửi lên server mỗi request, có expiry
   - **sessionStorage:** 5MB+, chỉ tồn tại trong session, không gửi lên server
   - **localStorage:** 5MB+, tồn tại vĩnh viễn, không gửi lên server

6. **Khác nhau giữa `<script>`, `<script async>` và `<script defer>`?**
   - **script:** Tải và thực thi ngay lập tức, chặn hiển thị trang
   - **async:** Tải song song với HTML, thực thi ngay khi tải xong
   - **defer:** Tải song song, nhưng chỉ thực thi sau khi HTML đã tải xong

7. **Tại sao nên đặt `<link>` trong thẻ `<head></head>` và đặt `<script>` sau thẻ `</body>`? Ngoại lệ khi nào?**
   - **link trong head:** Load CSS sớm tránh FOUC (Flash of Unstyled Content)
   - **script cuối body:** Không block render, tải sau khi có DOM
   - **Ngoại lệ:** Script cần thực thi sớm hoặc có async/defer

8. **Semantic HTML là gì và tại sao nó quan trọng?**
   - Là HTML sử dụng các thẻ mang ý nghĩa rõ ràng (e.g., `<header>`, `<article>`, `<footer>`)
   - **Quan trọng vì:** 
     - Cải thiện SEO
     - Truy cập tốt hơn
     - Dễ bảo trì

### Hỏi về CSS

1. **Lợi / hại của việc sử dụng External Style Sheets?**
   - **Lợi:** Tái sử dụng, cache, dễ maintain
   - **Hại:** Thêm HTTP request, có thể block rendering

2. **Khác nhau giữa Class selector và Id selector?**
   - **Class:** Dùng nhiều lần, độ ưu tiên thấp hơn
   - **ID:** Unique, độ ưu tiên cao hơn

3. **`z-index` dùng để làm gì?**
   - Kiểm soát thứ tự xếp chồng các element
   - Chỉ hoạt động với position không phải static

4. **Tại sao `@import` chỉ có thể sử dụng ở đầu file?**
   - Đảm bảo thứ tự load CSS đúng
   - Tránh blocking render không cần thiết

5. **CSS Grid và Flexbox khác nhau như thế nào?**
   - **CSS Grid:** Thiết kế 2 chiều (hàng và cột), tốt cho bố cục phức tạp
   - **Flexbox:** Thiết kế 1 chiều (hàng hoặc cột), phù hợp căn chỉnh nội dung

6. **CSS Module là gì và khi nào nên dùng?**
   - CSS Module là cách viết CSS giúp tạo các lớp CSS có phạm vi cục bộ (local)
   - Dùng khi dự án lớn hoặc khi cần tránh xung đột CSS

7. **Các đơn vị CSS thường dùng?**
   - **px:** Dùng để cố định kích thước
   - **%:** Tỷ lệ theo phần tử cha, dùng cho layout
   - **em:** Kích thước dựa trên font-size của phần tử cha
   - **rem:** Kích thước dựa trên font-size của root (html)
   - **vw, vh:** Tỷ lệ theo chiều rộng và chiều cao của viewport

### Hỏi về Javascript

1. **Ý nghĩa của biến `this`?**
   - Context của function hiện tại, phụ thuộc vào cách function được gọi

2. **Khác nhau giữa null, undefined hoặc chưa khai báo?**
   - **undefined:** Biến đã khai báo nhưng chưa gán giá trị
   - **null:** Giá trị rỗng được gán có chủ đích
   - **Chưa khai báo:** ReferenceError khi truy cập

3. **Javascript closure là gì?**
   - Là một hàm có thể ghi nhớ và truy cập biến từ phạm vi bên ngoài.

4. **ES6 `yield` là gì?**
   - Dùng trong generator function, tạm dừng hàm và trả về giá trị tại điểm dừng.

5. **ES6 `function*` là gì?**
   - Generator function có thể tạm dừng và tiếp tục thực thi nhờ `yield`.

6. **Khác biệt của arrow function?**
   - Không có `this` riêng, không có `arguments`, cú pháp ngắn gọn.

7. **Phân biệt `let`, `const`, `var` khi nào dùng?**
   - **let:** Biến có thể thay đổi giá trị, phạm vi khối.
   - **const:** Biến không thay đổi giá trị, phạm vi khối.
   - **var:** Phạm vi hàm, không nên sử dụng.

8. **Promise trong JS là gì?**
   - Là một đối tượng đại diện cho giá trị có thể có trong tương lai, có 3 trạng thái: Pending, Resolved (Fulfilled), Rejected.

### Hỏi về Performance

1. **Công cụ kiểm tra lỗi về hiệu suất tải trên trình duyệt?**
   - Chrome DevTools, Lighthouse

### Hỏi về Network

1. **Tại sao lưu resource (js/css/…) trên nhiều domain sẽ tốt hơn?**
   - Giảm tải đồng thời, tăng phân tán, và tận dụng cache.

2. **HTTP action là gì?**
   - Các phương thức dùng trong giao tiếp giữa client và server: `GET`, `POST`, `PUT`, `DELETE`, `PATCH`.
