

---

#  **BỘ 15 CÂU HỎI REACT (TỔNG HỢP)**

---

## **1. Trong React, useEffect với dependency array rỗng [] sẽ chạy bao nhiêu lần **

A. Chạy sau mỗi lần render
B. Chạy đúng một lần khi component mount
C. Chạy mỗi khi state thay đổi
D. Không bao giờ chạy

---

## **2. useEffect với dependency [count] sẽ chạy khi nào?**

A. Chỉ trong lần render đầu tiên
B. Mỗi lần component render (nếu không có dependency)
C. Chỉ khi state `count` đổi
D. Chỉ khi state `input` đổi

---

## **3. Điều gì xảy ra nếu bỏ mảng dependency trong useEffect?**

A. Chạy một lần duy nhất khi mount
B. Chạy sau mỗi lần render
C. Không chạy
D. Lỗi ngay lập tức

---

## **4. Nếu gọi setCount(count + 1) hai lần liên tiếp, count sẽ là?**

A. Tăng 1
B. Tăng 2
C. Không đổi
D. Kết quả ngẫu nhiên

---

## **5. Cách nào đảm bảo tăng count đúng khi gọi nhiều lần trong cùng 1 render?**

A. setCount(count + 1)
B. setCount(prev => prev + 1)
C. setCount(() => count + 2)
D. setCount(count++)

---

## **6. useEffect với mảng rỗng [] sẽ chạy khi nào?**

A. Mỗi lần component update
B. Chỉ 1 lần khi component mount
C. Khi component unmount
D. Code gây lỗi

---

## **7. Đây có phải cú pháp đúng để cleanup trong useEffect không?**

```js
useEffect(() => {
    const timer = setTimeout(() => console.log("Hello"), 1000);
    return () => clearTimeout(timer);
}, []);
```

A. Đúng
B. Sai, cần try-catch
C. Sai, cleanup phải return Promise
D. Sai, setTimeout phải chạy trong useState

---

## **8. Điều gì xảy ra với code sau?**

```js
const [count, setCount] = useState(0);
useEffect(() => {
    setCount(count + 1);
}, [count]);
```

A. Tăng count vô hạn
B. Lỗi crash ứng dụng
C. Tăng 1 lần duy nhất
D. Chỉ update khi count thay đổi

---

## **9. React xử lý DOM event như thế nào?**

A. Dùng event lowercase và handler dạng string
B. Dùng camelCase và handler dạng function
C. Dùng jQuery để bind event
D. Không hỗ trợ DOM event

---

## **10. Sự khác nhau giữa onClick và onClickCapture?**

A. onClickCapture chỉ dùng cho button
B. onClickCapture chạy ở bubbling
C. onClickCapture chạy ở capture phase
D. onClickCapture luôn chặn sự kiện

---

## **11. Lifecycle nào chạy ngay sau khi component được mount?**

A. componentWillUnmount
B. componentDidUpdate
C. componentDidMount
D. getSnapshotBeforeUpdate

---

## **12. Điều gì xảy ra trong component sau?**

```js
class Demo extends React.Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
    this.setState({ count: 1 });
  }
  render() {
    return <div>{this.state.count}</div>;
  }
}
```

A. Render 1
B. Render 0
C. Vòng lặp render vô hạn
D. Lỗi setState trong constructor

---

## **13. Bạn dùng lifecycle nào để cleanup trước khi component rời DOM?**

A. componentDidMount
B. componentDidUpdate
C. componentWillUnmount
D. shouldComponentUpdate

---

## **14. useNavigate trong React Router làm gì?**

A. Điều hướng trang bằng code
B. Render route theo điều kiện
C. Theo dõi lịch sử trình duyệt
D. Parse query trên URL

---

## **15. useParams trong React Router dùng để làm gì?**

A. Định nghĩa path
B. Lấy giá trị động từ URL
C. Validate form
D. Quản lý state component

---

Dưới đây là **bộ đáp án đầy đủ – chính xác 100% – cho 15 câu hỏi React của bạn**.

---

# **ĐÁP ÁN BỘ 15 CÂU HỎI REACT**

---

## **1. useEffect với dependency [] chạy bao nhiêu lần?**

 **Đáp án: B. Chạy đúng một lần khi component mount**

---

## **2. useEffect với dependency [count] sẽ chạy khi nào?**

 **Đáp án: C. Chỉ khi state `count` đổi**

---

## **3. Nếu bỏ dependency array trong useEffect?**

 **Đáp án: B. Chạy sau mỗi lần render**

---

## **4. Gọi setCount(count + 1) 2 lần liên tiếp → count sẽ?**

 **Đáp án: A. Tăng 1**

(Do React batching + cùng đọc 1 giá trị count cũ)

---

## **5. Cách tăng count đúng khi gọi nhiều lần?**

 **Đáp án: B. setCount(prev => prev + 1)**

---

## **6. useEffect([]) chạy khi nào?**

 **Đáp án: B. Chỉ 1 lần khi component mount**

---

## **7. Cú pháp cleanup trong useEffect này đúng không?**

 **Đáp án: A. Đúng**

---

## **8. Điều gì xảy ra?**

```js
useEffect(() => {
  setCount(count + 1);
}, [count]);
```

 **Đáp án: A. Tăng count vô hạn**

---

## **9. React xử lý DOM event như thế nào?**

 **Đáp án: B. Dùng camelCase và handler dạng function**

---

## **10. onClick vs onClickCapture khác nhau thế nào?**

 **Đáp án: C. onClickCapture chạy ở capture phase**

---

## **11. Lifecycle chạy ngay sau khi mount?**

 **Đáp án: C. componentDidMount**

---

## **12. Điều gì xảy ra trong class Demo?**

 **Đáp án: A. Render 1**

(setState trong constructor sẽ merge state ngay lập tức)

---

## **13. Lifecycle dùng để cleanup trước khi rời DOM?**

 **Đáp án: C. componentWillUnmount**

---

## **14. useNavigate dùng để làm gì?**

 **Đáp án: A. Điều hướng trang bằng code**

---

## **15. useParams dùng để làm gì?**

 **Đáp án: B. Lấy giá trị động từ URL**

---

