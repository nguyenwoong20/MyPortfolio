---
title: "Bài 9 - Kiểu Dữ Liệu Boolean - Logic Đúng/Sai Trong JavaScript"
slug: "bai-9-kieu-du-lieu-boolean"
date: 2025-09-28T13:00:00+07:00
categories: ["JavaScript Series", "JavaScript Cơ Bản"]
tags: ["javascript-basic", "boolean", "logic", "datatypes"]
series: ["JavaScript Basic"]
series_order: 9
draft: false
image: "https://img.youtube.com/vi/2Uvl-lJ9fBY/maxresdefault.jpg"
author: "Code Thu"
weight: 9
summary: "Tìm hiểu về kiểu dữ liệu Boolean và các phép toán logic trong JavaScript - Nền tảng cho điều kiện"
---

## 🎥 Video hướng dẫn chi tiết
**Nguồn:** [Khóa học JavaScript - Kteam](https://www.youtube.com/playlist?list=PL33lvabfss1ywJRoh40x9fmAfgbI1hpVX)
{{< youtube 2Uvl-lJ9fBY >}}

---

## 1. Boolean trong JavaScript

**Boolean** là kiểu dữ liệu logic chỉ có 2 giá trị:
- `true` - Đúng
- `false` - Sai

## 2. Cách tạo Boolean

### Trực tiếp:
```javascript
let isActive = true;
let isComplete = false;
console.log(typeof isActive);  // "boolean"
```

### Từ so sánh:
```javascript
let age = 25, minAge = 18;
let isAdult = age >= minAge;    // true
let isChild = age < minAge;     // false
```

### Từ hàm Boolean():
```javascript
console.log(Boolean(1));       // true
console.log(Boolean(0));       // false
console.log(Boolean("hello")); // true
console.log(Boolean(""));      // false
```

## 3. Truthy và Falsy Values

### Falsy Values (luôn là `false`):
```javascript
console.log(Boolean(false));     // false
console.log(Boolean(0));         // false
console.log(Boolean(""));        // false
console.log(Boolean(null));      // false
console.log(Boolean(undefined)); // false
console.log(Boolean(NaN));       // false
```

### Truthy Values (tất cả còn lại):
```javascript
console.log(Boolean(1));         // true
console.log(Boolean("hello"));   // true
console.log(Boolean([]));        // true
```

## 4. Toán tử Logic

### AND (&&) - Cả hai phải đúng:
```javascript
let age = 25, hasLicense = true;
let canDrive = age >= 18 && hasLicense;  // true
```

### OR (||) - Một trong hai đúng:
```javascript
let isWeekend = false, isHoliday = true;
let canRest = isWeekend || isHoliday;    // true

// Default values
let userName = null;
let displayName = userName || "Khách";  // "Khách"
```

### NOT (!) - Đảo ngược:
```javascript
let isLoggedIn = false;
let needsLogin = !isLoggedIn;  // true

// Chuyển về boolean
console.log(!!"hello");  // true
console.log(!!0);        // false
```

## 5. Short-circuit Evaluation

### && - Dừng khi gặp falsy:
```javascript
let user = { name: "John", profile: { email: "john@example.com" } };

// Safe navigation
console.log(user && user.profile && user.profile.email); // "john@example.com"

// Conditional execution
let isAdmin = true;
isAdmin && console.log("Welcome admin!");
```

### || - Dừng khi gặp truthy:
```javascript
function greet(name) {
    name = name || "Khách";  // Default value
    console.log(`Xin chào, ${name}!`);
}

greet("John");    // "Xin chào, John!"
greet();          // "Xin chào, Khách!"
```

## 6. So sánh với các toán tử

### == vs ===:
```javascript
// Loose equality (==) - Type coercion  
console.log(true == 1);        // true
console.log(false == 0);       // true

// Strict equality (===) - No type coercion
console.log(true === 1);       // false
console.log(true === true);    // true

// Best practice: Always use ===
let isComplete = true;
if (isComplete === true) {  // ✅ Good
    console.log("Task completed");
}
```

## 7. Bài tập nhỏ

Validate form đăng ký:
```javascript
function validateUser(userData) {
    let email = userData.email || "";
    let password = userData.password || "";
    let age = userData.age || 0;
    let agreeTerms = userData.agreeTerms || false;
    
    let validEmail = email.includes("@") && email.length >= 5;
    let validPassword = password.length >= 8;
    let validAge = age >= 13 && age <= 120;
    let termsAccepted = agreeTerms === true;
    
    let isValid = validEmail && validPassword && validAge && termsAccepted;
    
    return {
        isValid: isValid,
        checks: { validEmail, validPassword, validAge, termsAccepted }
    };
}

let testUser = {
    email: "user@example.com",
    password: "MyPass123",
    age: 25,
    agreeTerms: true
};

console.log(validateUser(testUser));
```

## Chốt lại:

Bài 9 giúp bạn hiểu về kiểu dữ liệu Boolean với 2 giá trị `true`/`false`, Truthy/Falsy values, các toán tử logic (`&&`, `||`, `!`), Short-circuit Evaluation, và sự khác biệt giữa `==` và `===` trong so sánh Boolean.

---

### 📚 Bài tiếp theo
👉 [**Bài 10: Null và Undefined**](/MyPortfolio/p/bai-10-null-undefined/) - Tìm hiểu sự khác biệt giữa null và undefined trong JavaScript!
