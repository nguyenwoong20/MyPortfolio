---
title: "Bài 10 - Null và Undefined - Hiểu Rõ Sự Khác Biệt"
slug: "bai-10-null-undefined"
date: 2025-09-28T13:30:00+07:00
categories: ["JavaScript Series", "JavaScript Cơ Bản"]
tags: ["javascript-basic", "null", "undefined", "datatypes"]
series: ["JavaScript Basic"]
series_order: 10
draft: false
image: "https://img.youtube.com/vi/CeM74bs91Sw/maxresdefault.jpg"
author: "Code Thu"
weight: 10
summary: "Tìm hiểu sự khác biệt quan trọng giữa null và undefined - Hai khái niệm dễ nhầm lẫn trong JavaScript"
---

## 🎥 Video hướng dẫn chi tiết
**Nguồn:** [Khóa học JavaScript - Kteam](https://www.youtube.com/playlist?list=PL33lvabfss1ywJRoh40x9fmAfgbI1hpVX)
{{< youtube CeM74bs91Sw >}}

---

## 1. Null vs Undefined - Khái niệm

```javascript
// Undefined - hệ thống tự gán
let notAssigned;
console.log(notAssigned); // undefined

// Null - lập trình viên gán có chủ ý
let user = null;
console.log(user); // null

// So sánh
console.log(typeof undefined);  // "undefined"
console.log(typeof null);       // "object" (bug lịch sử!)
console.log(undefined == null);   // true
console.log(undefined === null);  // false
```

## 2. Khi nào xuất hiện?

### Undefined xuất hiện:
```javascript
// Biến chưa gán giá trị
let notAssigned;
console.log(notAssigned); // undefined

// Truy cập property không tồn tại
let obj = { name: "John" };
console.log(obj.age); // undefined

// Function không return
function noReturn() { let x = 5; }
console.log(noReturn()); // undefined
```

### Null được gán có chủ ý:
```javascript
// Khởi tạo biến sẽ chứa object sau
let user = null;

// Reset giá trị object
let data = { name: "John" };
data = null; // Xóa reference

// API response không có dữ liệu
function findUser(id) {
    return null; // Không tìm thấy
}
```

## 3. Cách kiểm tra

```javascript
let value1;
let value2 = null;

// Kiểm tra cụ thể
console.log(value1 === undefined);    // true
console.log(value2 === null);         // true

// Kiểm tra cả hai
console.log(value1 == null);          // true
console.log(value2 == null);          // true

// Nullish coalescing
console.log(value1 ?? "default");     // "default"
console.log(value2 ?? "default");     // "default"
```

## 4. Nullish Coalescing (??) vs Logical OR (||)

```javascript
let userName = "";
let userAge = 0;
let profile = null;

// Nullish coalescing (??) - chỉ thay null/undefined
console.log(userName ?? "Anonymous");    // "" (giữ nguyên)
console.log(userAge ?? 18);              // 0 (giữ nguyên)
console.log(profile ?? {});              // {} (thay thế null)

// Logical OR (||) - thay tất cả falsy values
console.log(userName || "Anonymous");    // "Anonymous"
console.log(userAge || 18);              // 18
```

## 5. Best Practices

```javascript
// ✅ Good practices
let user = null;              // Sẽ chứa object sau
let userList = [];            // Mảng rỗng thay vì null
let settings = {};            // Object rỗng thay vì null

// Function với default parameters
function createPost(title = "Untitled", author = null) {
    return {
        title,
        author: author ?? "Anonymous",
        createdAt: new Date()
    };
}

// Check parameters
function processUser(userData) {
    if (userData === null || userData === undefined) {
        throw new Error("User data is required");
    }
    return { id: userData.id, name: userData.name ?? "Unknown" };
}
```

## Chốt lại

1. **`undefined`**: Hệ thống tự gán khi biến chưa có giá trị
2. **`null`**: Lập trình viên gán có chủ ý để đại diện "không có đối tượng"
3. **Kiểm tra**: `===` cho specific, `== null` cho cả hai
4. **Nullish coalescing** (`??`): Chỉ thay thế null/undefined, giữ nguyên falsy values khác
5. **Best practice**: Dùng `null` cho object, `[]` cho array, `""` cho string

---

### 📚 Bài tiếp theo
👉 [**Bài 11: Câu lệnh điều kiện if-else, switch-case**](/MyPortfolio/p/bai-11-cau-lenh-dieu-kien/) - Học cách điều khiển luồng chương trình với các câu lệnh điều kiện!
