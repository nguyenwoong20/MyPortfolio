---
title: "Bài 1 - Bí Kíp Constructor Nâng Cao Trong Java"
date: 2025-09-22T13:30:00+07:00
categories: ["Java Series", "Java Nâng Cao"]
tags: ["java-advanced"]
series: ["Java Advanced"]
series_order: 1
slug: "bai-1-constructor-advanced"
draft: false
image: "https://img.youtube.com/vi/NqfY0cQQrhA/maxresdefault.jpg"
---

## 🎥 Video minh họa nguồn: YTB Code Thu
{{< youtube NqfY0cQQrhA >}}

---

## 1) Constructor Chaining
Gọi constructor này từ constructor khác trong cùng class.

```java
public class Student {
    private String name;
    private int age;
    private String address;

    public Student() {
        this("No Name", 0); // Gọi constructor 2 tham số
    }

    public Student(String name, int age) {
        this(name, age, "Unknown"); // Gọi constructor 3 tham số
    }

    public Student(String name, int age, String address) {
        this.name = name;
        this.age = age;
        this.address = address;
    }
}
```

## 2) Copy Constructor
Tạo đối tượng mới bằng cách copy từ đối tượng có sẵn.

```java
public class Point {
    private int x, y;

    public Point(int x, int y) {
        this.x = x;
        this.y = y;
    }

    // Copy constructor
    public Point(Point p) {
        this.x = p.x;
        this.y = p.y;
    }
}

Point p1 = new Point(10, 20);
Point p2 = new Point(p1); // Copy values từ p1
```

## 3) Private Constructor
Hạn chế tạo đối tượng, thường dùng trong Singleton Pattern.

```java
public class DatabaseConnection {
    private static DatabaseConnection instance;
    
    private DatabaseConnection() {
        // Private constructor
    }
    
    public static DatabaseConnection getInstance() {
        if (instance == null) {
            instance = new DatabaseConnection();
        }
        return instance;
    }
}
```

## 4) Constructor với Inheritance
Constructor của lớp cha luôn được gọi trước khi khởi tạo lớp con.

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
        super("Dog"); // Phải gọi constructor lớp cha
        this.name = name;
    }
}
```

## 5) Kết luận & cảm nhận
- Constructor chaining giúp code gọn gàng, tái sử dụng logic khởi tạo
- Copy constructor an toàn khi cần nhân bản đối tượng
- Private constructor là kỹ thuật quan trọng trong design pattern

## Tiếp theo: [Bài 2: Từ khóa this trong Java](/MyPortfolio/p/bai-2-this-keyword/)
