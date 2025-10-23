---
title: "Bài 3 - Biến và Hằng Số - Nơi Lưu Trữ Dữ Liệu"
slug: "bai-3-bien-va-hang-so-noi-luu-tru-du-lieu"
date: 2025-09-28T10:00:00+07:00
categories: ["JavaScript Series", "JavaScript Cơ Bản"]
tags: ["javascript-basic", "variables", "constants"]
series: ["JavaScript Basic"]
series_order: 3
draft: false
image: "https://img.youtube.com/vi/5S2UOHZE5M0/maxresdefault.jpg"
author: "Code Thu"
weight: 3
summary: "Tìm hiểu cách khai báo và sử dụng biến, hằng số trong JavaScript - Nền tảng để lưu trữ dữ liệu"
---

## 🎥 Video hướng dẫn chi tiết
**Nguồn:** [Khóa học JavaScript - Kteam](https://www.youtube.com/playlist?list=PL33lvabfss1ywJRoh40x9fmAfgbI1hpVX)
{{< youtube 5S2UOHZE5M0 >}}

---

## 1. Biến là gì?

**Biến (Variable)** là "hộp chứa" để lưu trữ dữ liệu trong chương trình.

## 2. Khai báo biến với let

```javascript
let name = "Code Thu";
let age = 25;
let isStudent = true;

console.log(name);     // "Code Thu"
console.log(age);      // 25
```

### Khai báo không gán giá trị:
```javascript
let userName;           // undefined
userName = "John Doe";  // Gán giá trị sau
```

## 3. Hằng số với const

**Hằng số (Constant)** là biến không thể thay đổi giá trị sau khi khai báo:

```javascript
const PI = 3.14159;
const COMPANY_NAME = "Tech Corp";

console.log(PI); // 3.14159

// ❌ Lỗi! Không thể thay đổi
PI = 3.14; // TypeError
```

## 4. Thay đổi giá trị biến

```javascript
let score = 0;
score = 10;        // Gán giá trị mới
score += 5;        // Cộng thêm 5
console.log(score); // 15
```

## 5. Các kiểu dữ liệu cơ bản

```javascript
// String (Chuỗi)
let message = "Hello World";
let template = `Template với ${message}`;

// Number (Số)
let age = 25;
let price = 99.99;

// Boolean (Đúng/Sai)
let isActive = true;
let isComplete = false;

// Undefined
let notDefined;
console.log(typeof notDefined); // "undefined"
```

## 6. Quy tắc đặt tên biến

**✅ Đúng:**
- `userName` (camelCase)  
- `isLoggedIn` (có ý nghĩa)  
- `totalPrice` (mô tả rõ ràng)  

**❌ Sai:**
- `123abc` (không bắt đầu bằng số)  
- `user-name` (không dùng dấu gạch ngang)  
- `class` (từ khóa dành riêng)  

## 7. Kiểm tra kiểu dữ liệu

```javascript
let name = "JavaScript";
let age = 25;
let isActive = true;

console.log(typeof name);     // "string"
console.log(typeof age);      // "number"
console.log(typeof isActive); // "boolean"
```

## 8. Bài tập nhỏ

Tạo file `student-info.js`:
```javascript
const STUDENT_ID = "SV001";
let studentName = "Nguyen Van A";
let currentGrade = 8.5;
let age = 20;

console.log("Mã SV:", STUDENT_ID);
console.log("Họ tên:", studentName);
console.log("Tuổi:", age);
console.log("Điểm TB:", currentGrade);
```

## Chốt lại:

Bài 3 giúp bạn hiểu cách khai báo và sử dụng biến (`let`) và hằng số (`const`) trong JavaScript, các kiểu dữ liệu cơ bản, quy tắc đặt tên biến, và cách kiểm tra kiểu dữ liệu với `typeof`.

---

### 📚 Bài tiếp theo
👉 [**Bài 4: Khởi tạo biến bằng var và let**](../bai-4-toan-tu-so-hoc/) - So sánh sự khác biệt giữa `var` và `let`, tại sao nên dùng `let`!
