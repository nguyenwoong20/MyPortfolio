---
title: "Bài 9 - Interface Trong Java - Bắt Buộc Phải Hiểu"
date: 2025-09-22T18:00:00+07:00
categories: ["Java Series", "Java Nâng Cao"]
tags: ["java-advanced", "oop"]
series: ["Java Advanced"]
series_order: 9
slug: "bai-9-interface"
draft: false
image: "https://img.youtube.com/vi/RbhNslWAQHo/maxresdefault.jpg"
---

## 🎥 Video minh họa nguồn: YTB Code Thu
{{< youtube RbhNslWAQHo >}}

---

## 1) Interface là gì?
- Là bản thiết kế cho class, định nghĩa các hành vi mà class phải thực hiện
- Chỉ chứa abstract methods và constants
- Class implement interface phải override tất cả methods

## 2) Cách khai báo và sử dụng
```java
public interface Animal {
    // Constants (mặc định là public static final)
    String TYPE = "Animal";
    
    // Abstract methods (mặc định là public abstract)
    void makeSound();
    void move();
}

class Dog implements Animal {
    @Override
    public void makeSound() {
        System.out.println("Woof!");
    }
    
    @Override
    public void move() {
        System.out.println("Running on 4 legs");
    }
}
```

## 3) Tại sao cần Interface?
- Đạt được 100% abstraction
- Hỗ trợ multiple inheritance
- Loose coupling (giảm sự phụ thuộc giữa các class)

```java
// Một class có thể implement nhiều interface
public class Bird implements Flyable, Walkable {
    @Override
    public void fly() {
        System.out.println("Flying...");
    }
    
    @Override
    public void walk() {
        System.out.println("Walking...");
    }
}
```

## 4) Default Methods (Java 8+)
```java
public interface Vehicle {
    void start();
    
    // Default method có implementation
    default void stop() {
        System.out.println("Vehicle stopping...");
    }
}
```

## Tiếp theo: [Bài 10: Xử lý ngoại lệ trong Java](/MyPortfolio/p/bai-10-exception/)
