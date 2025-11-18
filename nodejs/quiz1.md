
---

# **BỘ 15 CÂU NODE.JS CƠ BẢN – HACK NÃO NHẸ – DỄ LÚ**

---

## **1. File Node.js có scope mặc định là gì?**

A. Global
B. Module riêng
C. Window
D. Không có scope

**Đáp án: B**
**Giải thích:** Mỗi file trong Node.js là một Module Scope độc lập, không phải global.

---

## **2. Kết quả?**

```js
console.log(this);
```

A. global
B. {}
C. undefined
D. window

**Đáp án: B**
**Top-level this = module.exports = {}**.

---

## **3. Require code lần 2 sẽ…**

```js
require("./app");
require("./app");
```

A. Chạy lại file 2 lần
B. Chạy 1 lần, lần sau lấy từ cache
C. Chạy vô hạn
D. Lỗi

**Đáp án: B**
Node.js cache module => require lần 2 KHÔNG chạy lại.

---

## **4. Lệnh nào chạy ứng dụng Node.js?**

A. node start app.js
B. node app.js
C. npm app.js
D. node.run app

**Đáp án: B**

---

## **5. Thuộc tính nào chứa thư mục hiện tại của file?**

A. process.cwd()
B. __dirname
C. __filename
D. cwd.file

**Đáp án: B**
`__dirname` = thư mục chứa file hiện tại.

---

## **6. Node.js có phải ngôn ngữ lập trình không?**

A. Có
B. Không
C. Tùy phiên bản
D. Chỉ khi chạy TypeScript

**Đáp án: B**
Node.js là **runtime** để chạy JavaScript.

---

## **7. Module nào là built-in của Node.js?**

A. http
B. mysql
C. express
D. nodemon

**Đáp án: A**
mysql/express/nodemon đều do bên thứ 3 cung cấp.

---

## **8. Lệnh nào cài package local?**

A. npm add express
B. npm install express
C. node add express
D. npm run express

**Đáp án: B**

---

## **9. Kết quả?**

```js
console.log(typeof require);
```

A. string
B. object
C. function
D. undefined

**Đáp án: C**

---

## **10. fs.readFile là hàm gì?**

A. Đồng bộ
B. Bất đồng bộ
C. Blocking
D. synchronous

**Đáp án: B**
`fs.readFile` là async.

---

## **11. Đâu là package.json hợp lệ?**

A. File chứa danh sách dependency
B. File chứa script để chạy app
C. File metadata của project
D. Tất cả đáp án trên

**Đáp án: D**

---

## **12. Điều gì xảy ra?**

```js
console.log(__filename);
```

A. In ra tên thư mục
B. In ra file hiện tại
C. In ra file index.js
D. Lỗi

**Đáp án: B**

---

## **13. Lệnh gỡ một package?**

A. npm uninstall xx
B. npm remove xx
C. npm delete xx
D. npm rmnode xx

**Đáp án: A**
`npm uninstall <name>` chuẩn nhất.

---

## **14. Kết quả?**

```js
console.log(process.env.NODE_ENV);
```

A. development
B. undefined
C. test
D. tùy môi trường đang chạy

**Đáp án: D**

---

## **15. Lệnh xem danh sách package local?**

A. npm ls
B. npm show
C. npm run
D. node ls

**Đáp án: A**

---
