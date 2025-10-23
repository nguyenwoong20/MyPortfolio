---
title: "Bài 12 - Override và Overload Trong Java - Khác Nhau Thế Nào?"
date: 2025-09-22T21:00:00+07:00
categories: ["java-series", "java Nâng Cao"]
tags: ["java-advanced"]
series: ["Java Advanced"]
series_order: 12
slug: "bai-12-override-overload"
draft: false
image: "https://img.youtube.com/vi/F-3n_mzG4o8/maxresdefault.jpg"
---

## 🎥 Video minh họa nguồn: YTB Code Thu
{{< youtube F-3n_mzG4o8 >}}

---

## 1) Method Overloading
- Cùng tên method, khác tham số
- Xảy ra trong cùng một class
- Compile-time polymorphism

```java
public class Calculator {
    // Cộng 2 số nguyên
    public int add(int a, int b) {
        return a + b;
    }
    
    // Cộng 3 số nguyên
    public int add(int a, int b, int c) {
        return a + b + c;
    }
    
    // Cộng 2 số thực
    public double add(double a, double b) {
        return a + b;
    }
}
```

## 2) Method Overriding
- Ghi đè method của class cha
- Cùng tên, cùng tham số
- Runtime polymorphism

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

## 3) Quy tắc quan trọng

### 3.1. Overloading Rules
1. Khác số lượng tham số
```java
void print(int a)
void print(int a, int b)
```

2. Khác kiểu tham số
```java
void print(int a)
void print(String a)
```

3. Khác thứ tự tham số
```java
void print(int a, String b)
void print(String b, int a)
```

### 3.2. Overriding Rules
1. Method phải có cùng tên và tham số
2. Return type phải giống hoặc là subtype
3. Access modifier không được hẹp hơn
4. Không override static methods

```java
class Parent {
    public Number calculate() { return 0; }
}

class Child extends Parent {
    @Override
    public Integer calculate() { return 42; } // OK vì Integer extends Number
}
```

## 4) So sánh Overloading vs Overriding

### Overloading
- Cùng class
- Khác tham số
- Compile-time
- Không cần kế thừa
- Không dùng @Override

### Overriding
- Class cha-con
- Cùng tham số
- Runtime
- Cần kế thừa
- Dùng @Override

## 5) Best Practices

### Overloading
1. Đặt tên method rõ ràng
2. Không lạm dụng overload
3. Tham số phải có ý nghĩa khác nhau

### Overriding
1. Luôn dùng @Override
2. Không thay đổi hành vi cốt lõi
3. Gọi super khi cần
4. Giữ nguyên contract của method
