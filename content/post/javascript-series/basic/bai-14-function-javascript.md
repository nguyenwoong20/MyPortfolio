---
title: "Bài 14 - Function trong JavaScript"
slug: "bai-14-function-javascript"
date: 2025-09-27T09:00:00+07:00
categories: ["JavaScript Series", "JavaScript Cơ Bản"]
series: ["JavaScript cơ bản"]
series_order: 14
draft: false
video: "https://youtu.be/Gtt7-jbKROw"

image: "https://img.youtube.com/vi/WUFb_huPvtI/maxresdefault.jpg"
author: "Code Thu"
weight: 14
summary: "Function trong JavaScript - khối lệnh tái sử dụng, nền tảng quan trọng để viết chương trình hiệu quả."
---

## 🎥 Video hướng dẫn chi tiết
**Nguồn:** [Khóa học JavaScript - Kteam](https://www.youtube.com/playlist?list=PL33lvabfss1ywJRoh40x9fmAfgbI1hpVX)
{{< youtube HZoubQZ2RRU >}}

---

## 1. Function là gì?  
- Khối lệnh có thể tái sử dụng nhiều lần.  
- Thực hiện một nhiệm vụ cụ thể.  
- Có thể nhận **tham số (parameters)** và trả về **kết quả (return)**.  

---

## 2. Cú pháp khai báo  

```javascript
// Function thường
function sayHello() {
    console.log("Hello!");
}

// Arrow function (ES6)
const add = (a, b) => a + b;
```

### 3. Tham số và Return
```javascript
Copy code
function greet(name, age = 20) {
    return `Hi ${name}, ${age} tuổi!`;
}

greet("An");        // "Hi An, 20 tuổi!"
greet("Bình", 25);  // "Hi Bình, 25 tuổi!"
```

### 4. Phạm vi biến (Scope)
```javascript
Copy code
let global = "Biến toàn cục";

function demo() {
    let local = "Biến cục bộ";
    console.log(global); // OK
    return local;
}

console.log(global);  // OK
console.log(local);   // ❌ Lỗi
```

### 📚 Bài tiếp theo
👉 [**Bài 15: Function Nâng Cao - Higher-order & Callback**](/MyPortfolio/p/bai-15-function-nang-cao/) - Khám phá sức mạnh của Higher-order Functions và Callbacks trong JavaScript!
