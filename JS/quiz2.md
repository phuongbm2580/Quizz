

# **BỘ CÂU HỎI JAVASCRIPT (20 CÂU – MỨC ĐỘ: TRUNG BÌNH)**

## **1. Giá trị nào dưới đây là “falsy” trong JavaScript?**

A. `"false"`
B. `[]`
C. `{}`
D. `0`

---

## **2. Điều gì xảy ra khi so sánh `[] == []`?**

A. true
B. false
C. undefined
D. SyntaxError

---

## **3. Kết quả của `typeof NaN` là gì?**

A. NaN
B. number
C. undefined
D. object

---

## **4. Biến được khai báo bằng `let` có đặc điểm nào sau đây?**

A. Hoisting nhưng không thể sử dụng trước khi khai báo
B. Không được hoisting
C. Giống const
D. Tự động trở thành global

---

## **5. Kết quả của `"5" - 2` là gì?**

A. `"3"`
B. `3`
C. `"5-2"`
D. NaN

---

## **6. Kết quả của `"5" + 2` là gì?**

A. `"52"`
B. `7`
C. NaN
D. `"5+2"`

---

## **7. Điều gì xảy ra khi gọi hàm trước khi định nghĩa bằng function declaration?**

A. Lỗi ReferenceError
B. Chạy bình thường nhờ hoisting
C. Lỗi TypeError
D. Không hoạt động trong strict mode

---

## **8. Điều gì xảy ra khi gọi hàm được gán bằng function expression trước khi khai báo?**

A. Chạy bình thường
B. Lỗi TypeError: x is not a function
C. Lỗi SyntaxError
D. Trả về undefined

---

## **9. Kết quả của `null == undefined` là gì?**

A. true
B. false
C. NaN
D. Error

---

## **10. Kết quả của `typeof null` là gì?**

A. null
B. object
C. undefined
D. false

---

## **11. Trong JavaScript, object được truyền vào hàm theo kiểu nào?**

A. Truyền theo giá trị (pass by value)
B. Truyền theo tham chiếu (pass by reference)
C. Cả hai
D. Tùy trình duyệt

---

## **12. Điểm khác biệt giữa `==` và `===` là gì?**

A. `===` so sánh giá trị và kiểu dữ liệu
B. `==` so sánh nghiêm ngặt hơn
C. Cả hai đều giống nhau
D. `==` chỉ dùng cho số

---

## **13. Kết quả của biểu thức sau là gì?**

```js
console.log([] + {});
```

A. "[object Object]"
B. ""
C. "{}"
D. Error

---

## **14. Kết quả của biểu thức sau?**

```js
console.log({} + []);
```

A. "[object Object]"
B. "0"
C. NaN
D. ""

---

## **15. Kết quả của `Boolean(" ")` (một chuỗi có dấu cách)?**

A. true
B. false
C. NaN
D. undefined

---

## **16. `map()` khác `forEach()` ở điểm nào?**

A. `map` trả về mảng mới, `forEach` không trả về
B. `forEach` nhanh hơn map
C. map thay đổi mảng gốc, forEach thì không
D. Không có sự khác biệt

---

## **17. Spread operator (`...`) làm gì với object?**

A. Tạo bản sao nông (shallow copy)
B. Tạo bản sao sâu (deep copy)
C. Merge sâu 2 object
D. Loại bỏ key trùng

---

## **18. Kết quả của đoạn code sau?**

```js
let a = { x: 1 };
let b = a;
b.x = 5;
console.log(a.x);
```

A. 1
B. 5
C. undefined
D. Error

---

## **19. Promise có trạng thái nào sau đây?**

A. pending, resolved, finished
B. pending, fulfilled, rejected
C. processing, done
D. loading, success, error

---

## **20. `async function` luôn trả về điều gì?**

A. Giá trị trả về thông thường
B. Một callback
C. Một Promise
D. undefined

---

---



Tuyệt rồi! Mình sẽ làm **2 phần** như bạn yêu cầu:

---

# **PHẦN 1 — ĐÁP ÁN + GIẢI THÍCH CHI TIẾT CHO 20 CÂU TRƯỚC**

---

## **1. Giá trị nào là falsy?**

**Đáp án: D. 0**
Giải thích:
Các giá trị falsy gồm: `0`, `''`, `null`, `undefined`, `NaN`, `false`.

---

## **2. `[] == []`?**

**Đáp án: B. false**
Giải thích:
Hai array khác nhau => khác tham chiếu => so sánh bằng false.

---

## **3. typeof NaN?**

**Đáp án: B. number**
Giải thích:
NaN là “Not a Number” nhưng kiểu dữ liệu lại là number — đây là bug lịch sử của JS.

---

## **4. let được hoisting nhưng không dùng được trước khi khai báo?**

**Đáp án: A**
Giải thích:
`let` hoisting nhưng nằm trong **Temporal Dead Zone**, dùng trước sẽ lỗi ReferenceError.

---

## **5. "5" - 2?**

**Đáp án: B. 3**
Giải thích:
Toán tử trừ buộc chuỗi thành số → 5 - 2 = 3.

---

## **6. "5" + 2?**

**Đáp án: A. "52"**
Giải thích:
Toán tử + khi có chuỗi → nối chuỗi.

---

## **7. Function declaration gọi trước khi khai báo?**

**Đáp án: B. Chạy bình thường**
Giải thích:
Function declaration hoisting đầy đủ.

---

## **8. Function expression gọi trước khi khai báo?**

**Đáp án: B. Lỗi TypeError: x is not a function**
Giải thích:
Biến được hoisting nhưng chưa gán nên là undefined → undefined() → lỗi TypeError.

---

## **9. null == undefined?**

**Đáp án: A. true**
Giải thích:
Loose equality: null chỉ bằng undefined.

---

## **10. typeof null?**

**Đáp án: B. object**
Giải thích:
Lỗi lịch sử trong JS — được giữ lại vì backward compatibility.

---

## **11. Object truyền vào hàm?**

**Đáp án: B. pass by reference**
Giải thích:
Thực chất là pass **reference by value** nhưng hiểu đơn giản: thay đổi object → ảnh hưởng bản gốc.

---

## **12. == vs ===?**

**Đáp án: A**
Giải thích:
`===` so sánh cả kiểu và giá trị.

---

## **13. [] + {} ?**

**Đáp án: A. "[object Object]"**
Giải thích rút gọn:
`[]` → ""
`{}` → "[object Object]"
"" + "[object Object]" → "[object Object]"

---

## **14. {} + [] ?**

**Đáp án: D. ""**

Giải thích:
Trong context bắt đầu bằng `{}`, JS hiểu đây là block → bỏ qua block → `+[]` → 0 → "".

---

## **15. Boolean(" ")?**

**Đáp án: A. true**
Giải thích:
Chuỗi rỗng là falsy, nhưng `" "` chứa khoảng trắng → truthy.

---

## **16. map() vs forEach()?**

**Đáp án: A**
Giải thích:
map tạo mảng mới; forEach không trả về gì.

---

## **17. Spread operator với object?**

**Đáp án: A. Tạo shallow copy**
Giải thích:
Copy 1 cấp — các object lồng vẫn tham chiếu chung.

---

## **18. let b = a; b.x = 5; thì a.x?**

**Đáp án: B. 5**
Giải thích:
b tham chiếu cùng object với a.

---

## **19. Trạng thái Promise?**

**Đáp án: B**
pending → fulfilled → rejected

---

## **20. async function trả về gì?**

**Đáp án: C. Một Promise**
Giải thích:
Dù return 5 cũng sẽ trở thành Promise.resolve(5).

---

---


