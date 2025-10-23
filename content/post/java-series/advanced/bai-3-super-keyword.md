---
title: "Bài 3 - Thay đổi suy nghĩ về SUPER trong Java"
date: 2025-09-22T14:30:00+07:00
categories: ["Java Series", "Java Nâng Cao"]
tags: ["java-advanced"]
series: ["Java Advanced"]
series_order: 3
slug: "bai-3-super-keyword"
draft: false
image: "https://img.youtube.com/vi/mmgmrG6G-lI/maxresdefault.jpg"
---

## 🎥 Video minh họa nguồn: YTB Code Thu
{{< youtube mmgmrG6G-lI >}}

---

## 1) Từ khóa super là gì?
`super` dùng để tham chiếu đến lớp cha (superclass), cho phép:
- Gọi constructor của lớp cha
- Gọi method của lớp cha
- Truy cập thuộc tính của lớp cha

## 2) Gọi constructor lớp cha
```java
class Animal {
    private String type;
    
    public Animal(String type) {
        this.type = type;
    }
}

class Dog extends Animal {
    private String name;
    
    public Dog(String name) {
        super("Dog"); // Gọi constructor lớp Animal
        this.name = name;
    }
}
```

## 3) Gọi method lớp cha khi override
```java
class Animal {
    public void makeSound() {
        System.out.println("Some sound");
    }
}

class Dog extends Animal {
    @Override
    public void makeSound() {
        super.makeSound(); // Gọi method của lớp cha
        System.out.println("Woof!");
    }
}
```

## 4) Truy cập thuộc tính lớp cha
```java
class Animal {
    protected String type;
    
    public Animal(String type) {
        this.type = type;
    }
}

class Dog extends Animal {
    private String name;
    
    public Dog(String name) {
        super("Dog");
        this.name = name;
    }
    
    public void printInfo() {
        System.out.println("Type: " + super.type); // Truy cập biến lớp cha
        System.out.println("Name: " + this.name);
    }
}
```

## 5) Super với Constructor Chaining
```java
class Animal {
    protected String type;
    protected String color;
    
    public Animal(String type) {
        this(type, "Unknown"); // Constructor chaining trong lớp cha
    }
    
    public Animal(String type, String color) {
        this.type = type;
        this.color = color;
    }
}

class Dog extends Animal {
    private String name;
    
    public Dog(String name) {
        super("Dog"); // Gọi constructor 1 tham số của Animal
        this.name = name;
    }
    
    public Dog(String name, String color) {
        super("Dog", color); // Gọi constructor 2 tham số của Animal
        this.name = name;
    }
}
```

## 6) Khi nào dùng super?
1. **PHẢI** dùng khi override constructor của lớp cha
2. Khi muốn gọi method gốc từ lớp cha sau khi override
3. Khi cần truy cập thuộc tính của lớp cha bị che bởi lớp con

## 7) Kết luận & cảm nhận
- `super` là công cụ quan trọng trong kế thừa
- Giúp tận dụng code của lớp cha một cách hiệu quả
- Cần hiểu rõ để tránh lỗi khi override

## Tiếp theo: [Bài 4: Lập trình hướng đối tượng trong Java](/MyPortfolio/p/bai-4-oop-overview/)
