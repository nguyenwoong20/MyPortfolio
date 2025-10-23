---
title: "Bài 7 - Tính Đa Hình (Polymorphism) Trong Java"
date: 2025-09-22T16:30:00+07:00
categories: ["Java Series", "Java Nâng Cao"]
tags: ["java-advanced", "oop"]
series: ["Java Advanced"]
series_order: 7
slug: "bai-7-polymorphism"
draft: false
image: "https://img.youtube.com/vi/OfEYrSBovtw/maxresdefault.jpg"
---

## 🎥 Video minh họa nguồn: YTB Code Thu
{{< youtube OfEYrSBovtw >}}

---

## 1) Đa hình là gì?
Đa hình (Polymorphism) cho phép một đối tượng có nhiều "hình dạng" khác nhau:
- Một method có thể có nhiều cách thực hiện
- Một đối tượng có thể được xem như nhiều kiểu khác nhau

## 2) Compile-time Polymorphism (Method Overloading)

```java
public class Calculator {
    // Cùng tên method, khác tham số
    public int add(int a, int b) {
        return a + b;
    }
    
    public double add(double a, double b) {
        return a + b;
    }
    
    public int add(int a, int b, int c) {
        return a + b + c;
    }
}
```

## 3) Runtime Polymorphism (Method Overriding)

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

// Sử dụng
Animal animal1 = new Dog(); // Đa hình
Animal animal2 = new Cat(); // Đa hình

animal1.makeSound(); // "Woof!"
animal2.makeSound(); // "Meow!"
```

## 4) Upcasting & Downcasting

### 4.1. Upcasting
Chuyển đổi từ class con lên class cha (tự động)
```java
Dog dog = new Dog();
Animal animal = dog; // Upcasting
```

### 4.2. Downcasting
Chuyển đổi từ class cha xuống class con (cần kiểm tra)
```java
Animal animal = new Dog();
if (animal instanceof Dog) {
    Dog dog = (Dog) animal; // Downcasting
    dog.bark();
}
```

## 5) Đa hình với Interface

```java
interface Playable {
    void play();
}

class Guitar implements Playable {
    @Override
    public void play() {
        System.out.println("Playing guitar...");
    }
}

class Piano implements Playable {
    @Override
    public void play() {
        System.out.println("Playing piano...");
    }
}

// Sử dụng
Playable instrument1 = new Guitar();
Playable instrument2 = new Piano();

instrument1.play(); // "Playing guitar..."
instrument2.play(); // "Playing piano..."
```

## 6) Best Practices

### 6.1. Programming to Interface
```java
// Thay vì
ArrayList<String> list = new ArrayList<>();

// Nên dùng
List<String> list = new ArrayList<>();
```

### 6.2. Sử dụng @Override
```java
@Override // Giúp compiler kiểm tra
public void makeSound() {
    System.out.println("Woof!");
}
```

### 6.3. Kiểm tra type trước khi cast
```java
if (obj instanceof Dog) {
    Dog dog = (Dog) obj;
} else {
    // Xử lý trường hợp khác
}
```

## 7) Kết luận & cảm nhận
- Đa hình giúp code linh hoạt, dễ mở rộng
- Kết hợp với interface tạo code loosely coupled
- Cẩn thận với downcasting để tránh lỗi runtime

## Tiếp theo: [Bài 8: Abstract Class trong Java](/MyPortfolio/p/bai-8-abstract-class/)
