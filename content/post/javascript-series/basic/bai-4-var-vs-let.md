---
title: "Bài 4 - Khởi Tạo Biến Với var và let - Sự Khác Biệt Quan Trọng"
slug: "bai-4-toan-tu-so-hoc"
date: 2025-09-28T10:30:00+07:00
categories: ["JavaScript Series", "JavaScript Cơ Bản"]
tags: ["javascript-basic", "var", "let", "scope"]
series: ["JavaScript Basic"]
series_order: 4
draft: false
image: "https://img.youtube.com/vi/kfibc_7N69o/maxresdefault.jpg"
author: "Code Thu"
weight: 4
summary: "Tìm hiểu sự khác biệt giữa var và let, tại sao let được ưa chuộng hơn trong JavaScript hiện đại"
---

## 🎥 Video hướng dẫn chi tiết
**Nguồn:** [Khóa học JavaScript - Kteam](https://www.youtube.com/playlist?list=PL33lvabfss1ywJRoh40x9fmAfgbI1hpVX)
{{< youtube kfibc_7N69o >}}

---

## 1. Tại sao có var và let?

JavaScript có 3 cách khai báo biến:
- `var` - Cách cũ (ES5)
- `let` - Cách mới (ES6/ES2015) 
- `const` - Cho hằng số 

**Khuyến nghị:** Dùng `let` thay vì `var`

## 🤔 Tại sao có 2 cách khai báo biến?

JavaScript có **3 cách** khai báo biến:
- `var` - Cách **cũ** (ES5 và trước đó)
- `let` - Cách **mới** (ES6/ES2015)
- `const` - Cho **hằng số** (ES6/ES2015)

## 📊 So sánh var vs let

| Đặc điểm | `var` | `let` |
|----------|-------|-------|
| **Scope** | Function scope | Block scope |
| **Hoisting** | Có, với undefined | Có, nhưng TDZ |
| **Re-declaration** | Được phép | Không được |
| **Cập nhật giá trị** | Được phép | Được phép |
| **Khuyến nghị** | ❌ Không nên dùng | ✅ Nên dùng |

## 2. Function Scope vs Block Scope

### var - Function Scope:
```javascript
if (true) {
    var x = 1;
}
console.log(x); // 1 - Truy cập được!
```

### let - Block Scope:
```javascript
if (true) {
    let y = 1;
}
console.log(y); // ❌ Lỗi! y is not defined
```

## 3. Hoisting (Đưa lên đầu)

### var - Hoisting với undefined:
```javascript
console.log(varVariable); // undefined (không lỗi)
var varVariable = "Hello";
```

### let - Temporal Dead Zone:
```javascript
console.log(letVariable); // ❌ Lỗi!
let letVariable = "Hello";
```

## 🚫 3. Re-declaration (Khai báo lại)

### var - Cho phép khai báo lại
```javascript
var name = "John";
var name = "Jane";  // ✅ OK
console.log(name);  // "Jane"

var age = 25;
var age = 30;      // ✅ OK, không báo lỗi
console.log(age);  // 30
```

### let - Không cho phép khai báo lại
```javascript
let name = "John";
let name = "Jane";  // ❌ SyntaxError: Identifier 'name' has already been declared

let age = 25;
age = 30;          // ✅ OK - Chỉ cập nhật giá trị
console.log(age);  // 30
```

## 5. Vòng lặp - Ví dụ thực tế

### Vấn đề với var:
```javascript
for (var i = 0; i < 3; i++) {
    setTimeout(function() {
        console.log("var:", i); // In ra: 3, 3, 3
    }, 100);
}
```

### Giải pháp với let:
```javascript  
for (let i = 0; i < 3; i++) {
    setTimeout(function() {
        console.log("let:", i); // In ra: 0, 1, 2
    }, 100);
}
```

## 6. Best Practices

**Thứ tự ưu tiên:**
1. `const` - Cho giá trị không đổi
2. `let` - Cho biến thay đổi  
3. `var` - ❌ Tránh sử dụng

```javascript
// ✅ Tốt
const API_URL = "https://api.example.com";
let userName = "john";

// ❌ Tránh
var oldStyle = "avoid this";
```

## 7. Bài tập nhỏ

Tìm lỗi trong code:
```javascript
function buggyCode() {
    console.log(message); // Lỗi gì?
    let message = "Hello";
    
    if (true) {
        var x = 1;
        let y = 2;
    }
    
    console.log(x); // Có lỗi không?
    console.log(y); // Có lỗi không?
}
```

## Chốt lại:

Bài 4 giúp bạn hiểu sự khác biệt giữa `var` và `let`: `var` có function scope và hoisting với undefined, `let` có block scope và Temporal Dead Zone. Nên sử dụng `let`/`const` thay vì `var` để code an toàn và dễ debug hơn.

---

### 📚 Bài tiếp theo
👉 [**Bài 5: Toán tử gán và toán tử so sánh**](/MyPortfolio/p/bai-5-toan-tu-gan-so-sanh/)- Học cách thực hiện phép toán và so sánh trong JavaScript!
