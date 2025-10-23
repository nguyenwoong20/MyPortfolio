---
title: "Bài 4 - Lập Trình Hướng Đối Tượng (OOP) trong Java"
date: 2025-09-22T15:00:00+07:00
categories: ["Java Series", "Java Nâng Cao"]
tags: ["java-advanced", "oop"]
series: ["Java Advanced"]
series_order: 4
slug: "bai-4-oop-overview"
draft: false
image: "https://img.youtube.com/vi/IcYpk-Kf4Fo/maxresdefault.jpg"
---

## 🎥 Video minh họa nguồn: YTB Code Thu
{{< youtube IcYpk-Kf4Fo >}}

---

## 1) OOP là gì?
Lập trình hướng đối tượng (Object-Oriented Programming) là phương pháp lập trình:
- Xem mọi thứ như đối tượng (object)
- Mỗi đối tượng có thuộc tính (attributes) và hành vi (methods)
- Code được tổ chức thành các class có tính độc lập

## 2) 4 Trụ cột của OOP

### 2.1. Tính đóng gói (Encapsulation)
- Gói dữ liệu và phương thức xử lý vào một đơn vị
- Che giấu chi tiết bên trong, chỉ công khai những gì cần thiết

```java
public class BankAccount {
    private double balance; // Thuộc tính private
    
    public void deposit(double amount) { // Method public
        if (amount > 0) {
            balance += amount;
        }
    }
}
```

### 2.2. Tính kế thừa (Inheritance)
- Class con kế thừa thuộc tính và phương thức từ class cha
- Tái sử dụng và mở rộng code

```java
class Animal {
    protected String name;
    
    public void eat() {
        System.out.println("Eating...");
    }
}

class Dog extends Animal {
    public void bark() {
        System.out.println("Woof!");
    }
}
```

### 2.3. Tính đa hình (Polymorphism)
- Một hành động có thể thực hiện theo nhiều cách khác nhau
- Overriding và Overloading

```java
class Animal {
    public void makeSound() {
        System.out.println("Some sound");
    }
}

class Dog extends Animal {
    @Override
    public void makeSound() {
        System.out.println("Woof!");
    }
}

class Cat extends Animal {
    @Override
    public void makeSound() {
        System.out.println("Meow!");
    }
}
```

### 2.4. Tính trừu tượng (Abstraction)
- Ẩn chi tiết phức tạp, chỉ hiển thị tính năng cần thiết
- Sử dụng abstract class và interface

```java
abstract class Shape {
    abstract double calculateArea();
}

class Circle extends Shape {
    private double radius;
    
    @Override
    double calculateArea() {
        return Math.PI * radius * radius;
    }
}
```

## 3) Ưu điểm của OOP
1. Code có tổ chức, dễ bảo trì
2. Tái sử dụng code hiệu quả
3. Bảo mật tốt hơn nhờ tính đóng gói
4. Linh hoạt trong phát triển nhờ tính đa hình
5. Mô phỏng thực tế tốt hơn

## 4) Best Practices trong OOP
1. Tuân thủ nguyên tắc SOLID
2. Ưu tiên composition over inheritance
3. Program to interface, not implementation
4. Keep classes small and focused
5. Đặt tên class, method có ý nghĩa

## 5) Kết luận & cảm nhận
- OOP giúp tổ chức code theo cách tự nhiên, dễ hiểu
- 4 trụ cột OOP là nền tảng cho thiết kế phần mềm tốt
- Cần thời gian thực hành để nắm vững và áp dụng hiệu quả

## Tiếp theo: [Bài 5: Tính Kế thừa trong Java](/MyPortfolio/p/bai-5-inheritance/)
