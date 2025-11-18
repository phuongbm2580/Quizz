
---

#  **15 CÂU TỔNG HỢP BIỂU THỨC LẠ + KIỂU DỮ LIỆU + THUẬT TOÁN**

---

## **1. Kết quả của biểu thức sau?**

```js
console.log([,,,].length);
```

A. 0
B. 3
C. 1
D. undefined

---

## **2. Biểu thức này in ra gì?**

```js
console.log([1, 2, 3] + [4, 5, 6]);
```

A. [1,2,3,4,5,6]
B. "1,2,34,5,6"
C. "1,2,34,5,6"
D. "1,2,34,5,6"

---

## **3. Kết quả?**

```js
console.log(0.2 + 0.1 === 0.3);
```

A. true
B. false
C. undefined
D. Error

---

## **4. Tại sao?**

```js
console.log(10 == "2");
```

A. true
B. false
C. Error
D. undefined

---

## **5. Kiểu dữ liệu của kết quả?**

```js
console.log(typeof []);
```

A. "array"
B. "object"
C. "list"
D. "function"

---

## **6. Object tham chiếu:**

```js
let a = {n:1};
let b = a;
b.n = 9;
console.log(a.n);
```

A. 1
B. 9
C. undefined
D. Error

---

## **7. Deep copy bằng JSON?**

```js
let a = {x:{y:2}};
let b = JSON.parse(JSON.stringify(a));
b.x.y = 7;
console.log(a.x.y);
```

A. 2
B. 7
C. undefined
D. Error

---

## **8. Kết quả thuật toán filter prime?**

```js
function isPrime(n){
  if(n<2) return false;
  for(let i=2;i<=Math.sqrt(n);i++)
    if(n%i===0) return false;
  return true;
}
console.log([2,3,4,5,10,11].filter(isPrime));
```

A. [2,3,5,11]
B. [3,5,11]
C. [2,3,11]
D. [2,5,11]

---

## **9. Tìm max bằng reduce:**

```js
console.log([3,9,1,7].reduce((a,b)=>a>b?a:b));
```

A. 9
B. 7
C. 1
D. 3

---

## **10. Đếm ký tự nhiều nhất:**

```js
function count(s){
  let map={};
  for(let c of s) map[c]=(map[c]||0)+1;
  return Object.entries(map).sort((a,b)=>b[1]-a[1])[0][0];
}
console.log(count("abcccccdd"));
```

A. a
B. b
C. c
D. d

---

## **11. Kết quả Set unique?**

```js
console.log([...new Set([1,2,2,3,3,4])].length);
```

A. 4
B. 6
C. 3
D. 2

---

## **12. Gộp mảng sâu 2 cấp:**

```js
console.log([1,[2,[3,4]],5].flat(2));
```

A. [1,2,3,4,5]
B. [1,2,[3,4],5]
C. [1,[2,3,4],5]
D. Error

---

## **13. Tìm tổng lớn nhất của subarray (Kadane):**

```js
console.log((function(arr){
  let max=-Infinity, cur=0;
  for(let n of arr){
    cur=Math.max(n,cur+n);
    max=Math.max(max,cur);
  }
  return max;
})([-1,2,3,-2,5]));
```

A. 8
B. 7
C. 5
D. 3

---

## **14. Biểu thức “NaN trap”:**

```js
console.log(NaN === NaN);
```

A. true
B. false
C. undefined
D. Error

---

## **15. Array + number?**

```js
console.log([] - 1);
```

A. -1
B. NaN
C. 0
D. undefined

---

---


# **ĐÁP ÁN + GIẢI THÍCH CHI TIẾT**

---

## **1. `[,,,].length` → 3**

**Đáp án: B**

Giải thích:
`[ , , , ]` là array có **3 empty slots**, JS không đếm giá trị mà đếm slot → length = 3.

---

## **2. `[1,2,3] + [4,5,6]` → "1,2,34,5,6"**

**Đáp án: B** (các B–C–D đều giống để troll)

Giải thích:
`+` khi gặp array → ép sang string:

* `[1,2,3].toString()` → `"1,2,3"`
* `[4,5,6].toString()` → `"4,5,6"`

Rồi `"1,2,3" + "4,5,6"` → `"1,2,34,5,6"`.

---

## **3. `0.2 + 0.1 === 0.3` → false**

**Đáp án: B**

Giải thích:
Số thực trong JS dùng IEEE 754 → có lỗi chính xác:
`0.1 + 0.2 = 0.30000000000000004`.

---

## **4. `10 == "2"` → false**

**Đáp án: B**

Giải thích:
`==` ép kiểu: `"2"` → 2 → so sánh 10 == 2 → false.

---

## **5. `typeof []` → "object"**

**Đáp án: B**

Giải thích:
Array trong JS là object → typeof không phân biệt array.

---

## **6. Object reference**

```js
let a = {n:1};
let b = a;
b.n = 9;
```

**Đáp án: B**

Giải thích:
`a` và `b` trỏ chung 1 object.

---

## **7. Deep copy bằng JSON**

**Đáp án: A (2)**

Giải thích:
JSON stringify → tạo object mới hoàn toàn → thay đổi b không ảnh hưởng a.

---

## **8. Lọc số nguyên tố**

**Đáp án: A — [2,3,5,11]**

Giải thích đúng theo thuật toán.

---

## **9. Reduce max**

**Đáp án: A (9)**

Giải thích:
Duyệt max theo so sánh a > b ? a : b.

---

## **10. Đếm ký tự nhiều nhất: "c"**

**Đáp án: C**

---

## **11. Set unique length**

```js
[1,2,2,3,3,4]
```

→ unique = 1,2,3,4 → length = 4

**Đáp án: A**

---

## **12. flat(2)**

**Đáp án: A — [1,2,3,4,5]**

---

## **13. Kadane**

Array: `[-1,2,3,-2,5]`
Best subarray: `[2,3,-2,5]` → sum = 8

**Đáp án: A**

---

## **14. `NaN === NaN` → false**

**Đáp án: B**

Giải thích:
NaN không bao giờ bằng chính nó.

---

## **15. `[] - 1` → -1**

**Đáp án: A**

Giải thích:
`[]` → `""` → `0`
`0 - 1` = -1.

---

---

