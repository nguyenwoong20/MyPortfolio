---
title: "Bài 6 - Kiểu Dữ Liệu Số Number - Làm Chủ Số Học JavaScript"
slug: "bai-6-kieu-du-lieu-number"
date: 2025-09-28T11:30:00+07:00
categories: ["JavaScript Series", "JavaScript Cơ Bản"]
tags: ["javascript-basic", "number", "math", "datatypes"]
series: ["JavaScript Basic"]
series_order: 6
draft: false
image: "https://img.youtube.com/vi/bynuI8B2uho/maxresdefault.jpg"
author: "Code Thu"
weight: 6
summary: "Tìm hiểu sâu về kiểu dữ liệu Number trong JavaScript - Từ cơ bản đến nâng cao"
---

## 🎥 Video hướng dẫn chi tiết
**Nguồn:** [Khóa học JavaScript - Kteam](https://www.youtube.com/playlist?list=PL33lvabfss1ywJRoh40x9fmAfgbI1hpVX)
{{< youtube bynuI8B2uho >}}

---

## 🔢 Number trong JavaScript

**Number** là kiểu dữ liệu để biểu diễn **tất cả các loại số** trong JavaScript.

```javascript
let integer = 42;              // Số nguyên
let decimal = 3.14;            // Số thập phân
let negative = -17;            // Số âm

console.log(typeof integer);   // "number"
```

## 🚫 Giá trị đặc biệt

**NaN (Not a Number):**
```javascript
console.log(0 / 0);            // NaN
console.log("hello" * 5);      // NaN
console.log(isNaN(NaN));       // true
```

**Infinity:**
```javascript
console.log(1 / 0);            // Infinity
console.log(-1 / 0);           // -Infinity
```

## 🧮 Object Math

```javascript
console.log(Math.PI);          // 3.141592653589793
console.log(Math.round(4.7));  // 5 (làm tròn)
console.log(Math.floor(4.7));  // 4 (làm tròn xuống)
console.log(Math.ceil(4.7));   // 5 (làm tròn lên)
console.log(Math.max(1,2,3));  // 3
console.log(Math.min(1,2,3));  // 1
```

### Phương thức tính toán:
## 🔄 Chuyển đổi sang Number

```javascript
let str = "123";
console.log(Number(str));      // 123
console.log(parseInt("123px")); // 123 
console.log(parseFloat("3.14kg")); // 3.14

console.log(Number(true));     // 1
console.log(Number(false));    // 0
```

## 🏋️ Bài tập thực hành

```javascript
// Tính BMI
let weight = 70;    // kg
let height = 1.75;  // m
let bmi = weight / Math.pow(height, 2);
console.log("BMI:", bmi.toFixed(1));

// Số ngẫu nhiên từ 1-10
let random = Math.floor(Math.random() * 10) + 1;
console.log("Random:", random);
```

## 🏆 Tóm tắt

✅ **Number** là kiểu dữ liệu duy nhất cho số  
✅ **Math object** cung cấp hằng số và phương thức toán học  
✅ **NaN** và **Infinity** là giá trị đặc biệt  
✅ Chuyển đổi bằng `Number()`, `parseInt()`, `parseFloat()`

---

### 📚 Bài tiếp theo
👉 [**Bài 7: Khái quát kiểu dữ liệu Chuỗi (String)**](/MyPortfolio/p/bai-7-kieu-du-lieu-string/) - Tìm hiểu chi tiết về xử lý chuỗi trong JavaScript!
