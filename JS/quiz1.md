
---

# **BỘ CÂU HỎI JAVASCRIPT**

---

## **1. Điều gì xảy ra khi chạy đoạn code sau?**

```js
console.log([1, 2, 3] == "1,2,3");
```

A. true
B. false
C. NaN
D. undefined

**Đáp án: A. true**
**Giải thích:** `[1,2,3].toString()` → `"1,2,3"` → so sánh chuỗi `"1,2,3"` == `"1,2,3"` → true.

---

## **2. Kết quả của đoạn code sau là gì?**

```js
console.log([] == ![]);
```

A. true
B. false
C. TypeError
D. undefined

**Đáp án: A. true**
**Giải thích:**

* `![]` → false
* `[]` → `""` → `0`
* `false` → `0`
  → `0 == 0` → true.

---

## **3. Kết quả khi so sánh hai object giống nhau?**

```js
const a = { x: 1 };
const b = { x: 1 };
console.log(a == b);
```

A. true
B. false
C. undefined
D. Error

**Đáp án: B. false**
**Giải thích:** Object so sánh theo tham chiếu, không phải nội dung → khác địa chỉ → false.

---

## **4. Kết quả của setTimeout trong vòng lặp var?**

```js
for (var i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 0);
}
```

A. 0 1 2
B. 3 3 3
C. undefined undefined undefined
D. Lỗi

**Đáp án: B. 3 3 3**
**Giải thích:** `var` không có block scope → kết thúc vòng lặp `i = 3` → 3 lần in 3.

---

## **5. Thứ tự in ra màn hình của Promise?**

```js
console.log("A");
Promise.resolve().then(() => console.log("B"));
console.log("C");
```

A. A C B
B. A B C
C. B A C
D. C B A

**Đáp án: A. A C B**
**Giải thích:**
Sync chạy trước → A, C
Microtask chạy sau → B.

---

## **6. Hoisting trong function với var?**

```js
function test() {
  console.log(a);
  var a = 10;
}
test();
```

A. 10
B. undefined
C. ReferenceError
D. NaN

**Đáp án: B. undefined**
**Giải thích:** `var a` được hoisting → tồn tại nhưng chưa gán → undefined.

---

## **7. Destructuring với chuỗi?**

```js
const { length } = "Hello";
console.log(length);
```

A. undefined
B. Error
C. 5
D. NaN

**Đáp án: C. 5**
**Giải thích:** String được tạm "bọc" thành object → lấy được length = 5.

---

## **8. typeof kết quả của hàm không return?**

```js
console.log(typeof (function() {})());
```

A. object
B. function
C. undefined
D. string

**Đáp án: C. undefined**
**Giải thích:** Hàm không return → undefined → typeof undefined → "undefined".

---

## **9. Kết quả của map trên sparse array?**

```js
console.log(Array(3).map(x => 1));
```

A. [1, 1, 1]
B. []
C. [empty × 3]
D. Error

**Đáp án: C. [empty × 3]**
**Giải thích:** `Array(3)` tạo 3 slot trống, map không duyệt slot trống → giữ nguyên.

---

## **10. JSON: undefined vs null?**

Sự khác biệt khi stringify:

A. Cả hai đều biến mất
B. null biến mất, undefined giữ lại
C. undefined biến mất, null giữ lại
D. Cả hai giữ lại

**Đáp án: C. undefined biến mất, null giữ lại**
**Giải thích:** JSON không lưu undefined.

---

## **11. Kết quả của:**

```js
JSON.stringify({ a: undefined, b: null })
```

A. "{}"
B. "{"b":null}"
C. "{"a":undefined,"b":null}"
D. null

**Đáp án: B. "{"b":null}"**
**Giải thích:** undefined bị bỏ qua, null giữ lại.

---

## **12. Kết quả của biểu thức:**

```js
console.log(1 < 2 < 3);
```

A. true
B. false
C. undefined
D. Error

**Đáp án: A. true**
**Giải thích:**
1 < 2 → true
true → 1
1 < 3 → true.

---

## **13. Kết quả của biểu thức:**

```js
console.log(3 > 2 > 1);
```

A. true
B. false
C. undefined
D. NaN

**Đáp án: B. false**
**Giải thích:**
3 > 2 → true
true → 1
1 > 1 → false.

---

## **14. Kết quả của || và ??**

```js
console.log(null || "A");
console.log(null ?? "A");
```

A. A và null
B. A và A
C. null và A
D. A và undefined

**Đáp án: B. A và A**
**Giải thích:**
|| dùng falsy → null là falsy → trả về "A".
?? dùng nullish → null → trả về "A".

---

## **15. Kết quả Promise chain sau:**

```js
Promise.resolve(1)
  .then(x => x * 2)
  .then(x => Promise.reject("Error"))
  .then(x => console.log("Success"))
  .catch(err => console.log(err));
```

A. Success
B. Error
C. undefined
D. Không in gì

**Đáp án: B. Error**
**Giải thích:**
Promise bị reject → nhảy thẳng xuống catch → in "Error".

---


