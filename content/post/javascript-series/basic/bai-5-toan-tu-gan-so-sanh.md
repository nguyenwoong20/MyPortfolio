---
title: "Bài 5 - Toán Tử Gán và Toán Tử So Sánh - Phép Toán Cơ Bản"
slug: "bai-5-toan-tu-gan-so-sanh"
date: 2025-09-28T11:00:00+07:00
categories: ["JavaScript Series", "JavaScript Cơ Bản"]
tags: ["javascript-basic", "operators", "assignment", "comparison"]
series: ["JavaScript Basic"]
series_order: 5
draft: false
image: "https://img.youtube.com/vi/N2QqCxjz-hY/maxresdefault.jpg"
author: "Code Thu"
weight: 5
summary: "Tìm hiểu các toán tử gán và so sánh trong JavaScript - Nền tảng cho mọi phép tính và điều kiện"
---

## 🎥 Video hướng dẫn chi tiết
**Nguồn:** [Khóa học JavaScript - Kteam](https://www.youtube.com/playlist?list=PL33lvabfss1ywJRoh40x9fmAfgbI1hpVX)
{{< youtube N2QqCxjz-hY >}}

---

## 1. Toán tử số học

```javascript
let a = 10, b = 3;

console.log(a + b);    // 13 - Cộng
console.log(a - b);    // 7  - Trừ
console.log(a * b);    // 30 - Nhân
console.log(a / b);    // 3.33 - Chia
console.log(a % b);    // 1  - Chia lấy dư
console.log(a ** b);   // 1000 - Lũy thừa
```

### Toán tử tăng/giảm:
```javascript
let count = 5;
console.log(count++);  // 5 (dùng trước, tăng sau)
console.log(++count);  // 7 (tăng trước, dùng sau)
```

## 2. Toán tử gán

### Gán cơ bản:
```javascript
let x = 10;
let name = "John";
let isActive = true;
```

### Toán tử gán kết hợp:
```javascript
let score = 100;
score += 50;   // score = score + 50
score -= 30;   // score = score - 30
score *= 2;    // score = score * 2
score /= 4;    // score = score / 4
```

## 3. Toán tử so sánh

```javascript
let a = 5, b = "5", c = 10;

// So sánh giá trị
console.log(a == b);   // true (5 == "5")
console.log(a === b);  // false (khác kiểu)
console.log(a != b);   // false
console.log(a !== b);  // true

// So sánh lớn hơn, nhỏ hơn
console.log(a > c);    // false
console.log(a < c);    // true
console.log(a >= 5);   // true
console.log(a <= 10);  // true
```

## 4. Sự khác biệt `==` vs `===`

### `==` (Loose Equality):
```javascript
console.log(5 == "5");     // true (tự động chuyển đổi kiểu)
console.log(true == 1);    // true
console.log("" == 0);      // true
```

### `===` (Strict Equality) - Khuyên dùng:
```javascript
console.log(5 === "5");    // false (khác kiểu)
console.log(true === 1);   // false
console.log("" === 0);     // false
```

## 5. Thứ tự ưu tiên toán tử

```javascript
let result = 2 + 3 * 4;    // 14 (không phải 20)
let result2 = (2 + 3) * 4; // 20 (có dấu ngoặc)
```

**Thứ tự ưu tiên:** `()` → `**` → `*`, `/`, `%` → `+`, `-` → so sánh → `===` → gán

## 6. Bài tập nhỏ

Tính toán hóa đơn:
```javascript
const PRICE = 500000;
let quantity = 2;
let discount = 10; // %

let subtotal = PRICE * quantity;
let discountAmount = subtotal * (discount / 100);
let total = subtotal - discountAmount;

console.log("Tạm tính:", subtotal, "VND");
console.log("Giảm giá:", discountAmount, "VND");  
console.log("Tổng cộng:", total, "VND");
```

## Chốt lại:

Bài 5 giúp bạn hiểu các toán tử số học (`+`, `-`, `*`, `/`, `%`), toán tử gán (`=`, `+=`, `-=`), toán tử so sánh (`===`, `!==`, `>`, `<`), sự khác biệt giữa `==` và `===`, và thứ tự ưu tiên toán tử trong JavaScript.

---

### 📚 Bài tiếp theo
👉 [**Bài 6: Kiểu dữ liệu số Number**](/MyPortfolio/p/bai-6-kieu-du-lieu-number/) - Tìm hiểu chi tiết về số trong JavaScript!
