---
title: "Bài 3 - Làm chủ String trong Java"
slug: "bai-3-string"
date: 2025-09-22T10:00:00+07:00
categories: ["Java Series", "Java Cơ Bản"]
tags: ["java-basic"]
series: ["Java Basic"]
series_order: 3
draft: false
image: "https://img.youtube.com/vi/14MHZ23g0eI/maxresdefault.jpg"
---

## 🎥 Video minh họa nguồn: YTB Code Thu
{{< youtube 14MHZ23g0eI >}}

---

## 1) String là gì?
String là một kiểu tham chiếu (class) trong Java, dùng lưu chuỗi ký tự (text).

Bất cứ thứ gì nằm giữa cặp dấu ngoặc kép ("") đều là String.

Ví dụ:

```java
String msg = "Hello Code Thủ";
```

## 2) Tính bất biến (immutable)
String trong Java bất biến: Khi thay đổi giá trị, đối tượng mới được tạo, giá trị cũ không bị thay đổi.

Ví dụ:

```java
String s1 = "Java";
String s2 = s1;
s1 = "Hello";
System.out.println(s2); // vẫn in "Java"
```

## 3) Các thao tác phổ biến với String
Nối chuỗi (sử dụng toán tử +):

```java
String s = "Hello " + "Code Thủ";
System.out.println(s); // Hello Code Thủ
```

Nối chuỗi với biến/giá trị:

```java
int number = 123;
System.out.println("Code Thủ " + number); // Code Thủ 123
```

## 4) Một số phương thức hữu ích
- `.length()`: Độ dài chuỗi.
- `.toUpperCase()`, `.toLowerCase()`: Chuyển chuỗi sang chữ hoa/thường.
- `.indexOf()`: Vị trí đầu tiên tìm thấy ký tự/chuỗi con, -1 nếu không có.
- `.replace(old, new)`: Thay thế tất cả ký tự/chuỗi con phù hợp bằng chuỗi khác.
- `.trim()`: Loại bỏ khoảng trắng đầu/cuối chuỗi.
- `.isEmpty()`: Kiểm tra chuỗi có rỗng không.

```java
String name = "  Code Thủ  ";
System.out.println(name.trim().toUpperCase()); // CODE THỦ
```

## 5) So sánh String
Quan trọng: Không so sánh giá trị chuỗi bằng hai dấu == mà phải dùng `.equals()` hoặc `.equalsIgnoreCase()`.

```java
String a = "Java";
String b = "JAVA";
System.out.println(a.equals(b));          // false
System.out.println(a.equalsIgnoreCase(b)); // true
```

## 6) Kết luận & cảm nhận
- Video Code Thủ giúp mình hiểu sâu về bản chất "bất biến" của chuỗi, thao tác nối/chỉnh sửa, so sánh chuẩn không lỗi logic.

- Biết cách dùng method hữu ích của String giúp làm việc nhanh hơn và tránh bug khó đoán lúc kiểm tra điều kiện hoặc nhập xuất.

## Tiếp theo: [Bài 4 – Lớp (Class) và Constructor trong Java](/MyPortfolio/p/bai-4-class-constructor/)
