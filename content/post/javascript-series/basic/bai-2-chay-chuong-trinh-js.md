---
title: "Bài 2 - Chạy Chương Trình JavaScript Cơ Bản Bằng Node"
slug: "bai-2-chay-chuong-trinh-js"
date: 2025-09-28T09:30:00+07:00
categories: ["JavaScript Series", "JavaScript Cơ Bản"]
tags: ["javascript-basic", "nodejs", "hello-world"]
series: ["JavaScript Basic"]
series_order: 2
draft: false
image: "https://img.youtube.com/vi/cbZfmmIlzaU/maxresdefault.jpg"
author: "Code Thu"
weight: 2
summary: "Tạo và chạy chương trình JavaScript đầu tiên với NodeJS - Hello World và những khái niệm cơ bản"
---

## 🎥 Video hướng dẫn chi tiết
**Nguồn:** [Khóa học JavaScript - Kteam](https://www.youtube.com/playlist?list=PL33lvabfss1ywJRoh40x9fmAfgbI1hpVX)
{{< youtube cbZfmmIlzaU >}}

---

## 1. Tạo file JavaScript đầu tiên

Mở Terminal hoặc VS Code.

Lệnh tạo thư mục và di chuyển vào thư mục mới:
```bash
mkdir my-first-js
cd my-first-js
```

Tạo file mới: `hello.js`

## 2. Code Hello World đơn giản

```javascript
// In ra màn hình
console.log("Hello, JavaScript!");
console.log("Chào mừng bạn đến với NodeJS.");
```

## 3. Chạy file bằng NodeJS

Trong terminal, chạy:
```bash
node hello.js
```

Kết quả:
```
Hello, JavaScript!
Chào mừng bạn đến với NodeJS.
```

## 4. Sử dụng console.log

In bất cứ thứ gì lên màn hình console:
```javascript
console.log("Thông báo");
console.log(123);
console.log(true);
```

## 5. Thông tin hệ thống bằng process.version, process.platform

```javascript
console.log("Phiên bản NodeJS:", process.version);
console.log("OS:", process.platform);
```

## 6. Hướng dẫn chạy với REPL

Gõ lệnh `node` và thử trực tiếp:
```javascript
> console.log("Hello trực tiếp");
> 1 + 2
```

## 7. Debug nhanh

Nếu thấy lỗi về tên file, cú pháp hoặc biến chưa khai báo: kiểm tra lại chính xác tên file, dấu ngoặc, khai báo biến.

Đảm bảo file lưu dưới dạng `.js`.

## 8. Bài tập nhỏ

Tạo file `about-me.js`:
```javascript
console.log("Tên:", "Tên của bạn");
console.log("Tuổi:", 20);
console.log("Nghề nghiệp:", "Học lập trình");
```

Tạo file `calculator.js`:
```javascript
let a = 10, b = 3;
console.log("a + b =", a + b);
console.log("a - b =", a - b);
```

## Chốt lại:

Bài 2 giúp bạn làm chủ cách tạo & chạy file JavaScript đầu tiên bằng NodeJS, sử dụng console.log để xuất dữ liệu, thao tác và debug đơn giản, đặt nền móng cho các bài học kế tiếp.

---

### 📚 Bài tiếp theo
👉 [**Bài 3: Biến và Hằng số**](../bai-3-bien-va-hang-so-noi-luu-tru-du-lieu/) - Tìm hiểu cách lưu trữ và sử dụng dữ liệu trong JavaScript!
