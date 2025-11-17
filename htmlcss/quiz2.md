
#  **BỘ CÂU HỎI HTML – CSS**

---

## **1. Thuộc tính nào quyết định kích thước cuối cùng của phần tử khi “width” và “padding” đều được set, nhưng “box-sizing” không được khai báo?**

A. width
B. padding
C. content-box
D. width + padding + border

**Đáp án đúng:** D
**Giải thích:**
Mặc định là `box-sizing: content-box` → **tổng chiều rộng = width + padding + border**, rất dễ vượt layout.

---

## **2. Điều gì xảy ra khi một phần tử inline có `height: 100px`?**

A. Chiều cao tăng lên 100px
B. Không áp dụng, height bị bỏ qua
C. Inline chuyển thành block
D. Làm tăng line-height

**Đáp án đúng:** B
**Giải thích:**
Inline **không nhận height/width**, chỉ nhận padding.

---

## **3. Điều gì xảy ra khi khai báo cả `margin: auto` và `float: left`?**

A. margin auto căn giữa phần tử
B. float left ưu tiên, margin auto bị vô hiệu
C. Cả hai hoạt động bình thường
D. Trình duyệt lỗi và bỏ float

**Đáp án đúng:** B
**Giải thích:**
`float` phá vỡ cơ chế block centering → margin auto **không còn hiệu lực**.

---

## **4. Trong Flexbox, item nào sẽ giãn lớn nhất khi tất cả đều có `flex: 1` nhưng một item có `min-width: 300px`?**

A. Item có min-width
B. Item không có min-width
C. Tất cả giãn đều nhau
D. Tùy vào nội dung bên trong

**Đáp án đúng:** A
**Giải thích:**
Item có `min-width` **không thể nhỏ hơn 300px**, nên khi chia không gian nó trở nên “lấn át”.

---

## **5. Trong Grid, nếu một item đặt `grid-column: 2 / 1`, điều gì xảy ra?**

A. Hiển thị từ cột 2 sang 1 theo chiều ngược
B. Không hiển thị item
C. Trình duyệt tự đảo thành 1 / 2
D. Lỗi layout và Grid bị ngắt

**Đáp án đúng:** C
**Giải thích:**
Grid **tự động swap** giá trị → `1 / 2`.

---

## **6. Nếu một phần tử có `z-index: 9999` nhưng không có `position`, kết quả là gì?**

A. z-index vẫn hoạt động
B. z-index bị bỏ qua
C. Phần tử tự động thành relative
D. Chỉ hoạt động với inline elements

**Đáp án đúng:** B
**Giải thích:**
`z-index` chỉ có tác dụng với phần tử có `position` khác `static`.

---

## **7. Điều gì xảy ra khi set `overflow: hidden` và `position: sticky` cùng lúc?**

A. Sticky hoạt động bình thường
B. Sticky bị vô hiệu
C. Sticky hoạt động nhưng mất overflow
D. Cả hai hoạt động theo thứ tự

**Đáp án đúng:** B
**Giải thích:**
Một ancestor có `overflow: hidden/auto/scroll` → **làm sticky bị vô hiệu hóa**.

---

## **8. Trong Flexbox, thuộc tính nào kiểm soát khoảng cách *giữa* các items mà không tạo khoảng bên ngoài container?**

A. margin
B. padding
C. gap
D. space-between

**Đáp án đúng:** C
**Giải thích:**
`gap` = “khoảng giữa phần tử”, không phải margin.

---

## **9. HTML: thuộc tính `defer` và `async` khác nhau điểm nào?**

A. async đảm bảo chạy đúng thứ tự, defer thì không
B. defer chạy sau khi HTML parse xong, async chạy bất kỳ khi tải xong
C. async chặn render, defer không chặn
D. defer chỉ dùng cho module script

**Đáp án đúng:** B
**Giải thích:**
`defer`: chạy **sau khi DOM parse xong**
`async`: tải xong là chạy ngay → dễ chạy **trước DOM**.

---

## **10. Trong Grid, điều gì xảy ra nếu tổng số cột khai báo nhỏ hơn số items?**

A. Items dư bị ẩn
B. Items dư đè lên nhau
C. Items dư tự động nhảy xuống hàng mới
D. Trình duyệt báo lỗi

**Đáp án đúng:** C
**Giải thích:**
Grid tự tạo **hàng auto** cho items dư.

---

## **11. Điều gì xảy ra khi sử dụng `flex: 0 0 auto`?**

A. Item không được giãn
B. Item không bị co lại
C. Item giữ nguyên kích thước nội dung
D. Tất cả đáp án trên

**Đáp án đúng:** D
**Giải thích:**
`flex: 0 0 auto` →

* grow = 0 → không giãn
* shrink = 0 → không co
* basis = auto → theo content
  → “bất động” item.

---

## **12. Trong CSS, điều gì xảy ra nếu khai báo 2 class có thuộc tính trùng nhau trên cùng một thẻ?**

```html
<div class="a b"></div>
```

```css
.a { color: red; }
.b { color: blue; }
```

A. Màu đỏ
B. Màu xanh
C. Tùy vào HTML
D. Tùy trình duyệt

**Đáp án đúng:** B
**Giải thích:**
Class viết sau trong CSS → **ưu tiên hơn** (Cascading).
Ở đây `.b` override `.a`.

---

