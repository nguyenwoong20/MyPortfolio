---
title: "Bài 15 - Function Nâng Cao - Higher-order & Callback"
slug: "bai-15-function-nang-cao"
date: 2025-09-28T15:30:00+07:00
categories: ["JavaScript Series", "JavaScript Cơ Bản"]
tags: ["javascript-basic", "higher-order-function", "callback", "closure"]
series: ["JavaScript Basic"]
series_order: 15
draft: false
image: "https://img.youtube.com/vi/pkuC_jsH1T8/maxresdefault.jpg"
author: "Code Thu"
weight: 15
summary: "Khám phá sức mạnh của Higher-order Functions và Callbacks trong JavaScript"
---

## 🎥 Video hướng dẫn chi tiết
**Nguồn:** [Khóa học JavaScript - Kteam](https://www.youtube.com/playlist?list=PL33lvabfss1ywJRoh40x9fmAfgbI1hpVX)
{{< youtube pkuC_jsH1T8 >}}

---

## 1. Higher-order Function & Callback

```javascript
// Higher-order function: nhận function làm parameter
function greet(name, callback) {
    console.log("Xin chào, " + name);
    callback();
}

function sayGoodbye() {
    console.log("Tạm biệt!");
}

greet("An", sayGoodbye);
// Xin chào, An
// Tạm biệt!
```

## 2. Array Methods với Callback

```javascript
let numbers = [1, 2, 3, 4, 5];

// forEach - lặp qua mảng
numbers.forEach(num => console.log(num * 2));

// map - transform mảng
let doubled = numbers.map(num => num * 2);
console.log(doubled); // [2, 4, 6, 8, 10]

// filter - lọc mảng
let evenNumbers = numbers.filter(num => num % 2 === 0);
console.log(evenNumbers); // [2, 4]

// reduce - tính tổng
let sum = numbers.reduce((total, num) => total + num, 0);
console.log(sum); // 15
```

## 3. Closure - Bao đóng

```javascript
// Function con truy cập biến function cha
function outerFunction(x) {
    let outerVar = x;
    
    function innerFunction(y) {
        return outerVar + y; // Truy cập được outerVar
    }
    
    return innerFunction;
}

let addFive = outerFunction(5);
console.log(addFive(3)); // 8

// Counter với closure
function createCounter() {
    let count = 0;
    return function() {
        count++;
        return count;
    };
}

let counter = createCounter();
console.log(counter()); // 1
console.log(counter()); // 2
```

## 4. Function Factory

```javascript
// Tạo functions với closure
function createMultiplier(multiplier) {
    return function(x) {
        return x * multiplier;
    };
}

let double = createMultiplier(2);
let triple = createMultiplier(3);

console.log(double(5)); // 10
console.log(triple(5)); // 15

// Greeter factory
function createGreeter(greeting) {
    return function(name) {
        return greeting + ", " + name + "!";
    };
}

let sayHello = createGreeter("Xin chào");
console.log(sayHello("An")); // Xin chào, An!
```

## Chốt lại

1. **Higher-order function**: Nhận function làm parameter hoặc return function
2. **Callback**: Function được truyền vào function khác để thực thi
3. **Array methods**: `forEach`, `map`, `filter`, `reduce` - xử lý mảng hiệu quả
4. **Closure**: Function con có thể truy cập biến của function cha
5. **Function factory**: Sử dụng closure để tạo các function có behavior tương tự

---

### 📚 Bài tiếp theo
👉 [**Bài 16: Đệ quy trong JavaScript**](../bai-16-de-quy/) - Kỹ thuật giải quyết vấn đề bằng chính nó!
