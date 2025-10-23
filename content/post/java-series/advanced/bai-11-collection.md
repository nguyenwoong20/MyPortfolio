---
title: "Bài 11 - Collection Framework Trong Java - Từ Array Đến ArrayList"
date: 2025-09-22T20:00:00+07:00
categories: ["Java Series", "Java Nâng Cao"]
tags: ["java-advanced"]
series: ["Java Advanced"]
series_order: 11
slug: "bai-11-collection"
draft: false
image: "https://img.youtube.com/vi/m4QD2ykLiiw/maxresdefault.jpg"
---

## 🎥 Video minh họa nguồn: YTB Code Thu
{{< youtube m4QD2ykLiiw >}}

---

## 1) Array và ArrayList
### 1.1. Array
```java
// Khai báo và khởi tạo
int[] numbers = new int[5];
String[] names = {"John", "Mary", "Tom"};

// Truy cập phần tử
numbers[0] = 10;
String firstPerson = names[0];
```

### 1.2. ArrayList
```java
ArrayList<String> list = new ArrayList<>();
list.add("Apple");
list.add("Banana");
list.remove(0);
System.out.println(list.get(0)); // Banana
```

## 2) List Interface
```java
// ArrayList - Truy cập nhanh
List<Integer> arrayList = new ArrayList<>();

// LinkedList - Thêm/xóa nhanh
List<Integer> linkedList = new LinkedList<>();

// Vector - Thread safe
List<Integer> vector = new Vector<>();
```

## 3) Set Interface
```java
// HashSet - Không cho phép trùng lặp
Set<String> hashSet = new HashSet<>();
hashSet.add("Apple");
hashSet.add("Apple"); // Không thêm được

// TreeSet - Sắp xếp tự động
Set<Integer> treeSet = new TreeSet<>();
treeSet.add(5);
treeSet.add(1);
treeSet.add(3);
System.out.println(treeSet); // [1, 3, 5]
```

## 4) Map Interface
```java
// HashMap
Map<String, Integer> ages = new HashMap<>();
ages.put("John", 25);
ages.put("Mary", 30);
System.out.println(ages.get("John")); // 25

// TreeMap - Sắp xếp theo key
Map<String, Double> scores = new TreeMap<>();
scores.put("Math", 8.5);
scores.put("English", 7.0);
```

## 5) Các thao tác phổ biến
```java
List<String> fruits = new ArrayList<>();

// Thêm phần tử
fruits.add("Apple");
fruits.add("Banana");

// Duyệt list
for(String fruit : fruits) {
    System.out.println(fruit);
}

// Sử dụng Iterator
Iterator<String> it = fruits.iterator();
while(it.hasNext()) {
    System.out.println(it.next());
}

// Sắp xếp
Collections.sort(fruits);

// Tìm kiếm
int index = fruits.indexOf("Apple");
```

## 6) So sánh hiệu năng
- ArrayList: Truy cập nhanh, thêm/xóa chậm
- LinkedList: Truy cập chậm, thêm/xóa nhanh
- HashSet: Tìm kiếm nhanh O(1)
- TreeSet: Tìm kiếm O(log n), tự động sắp xếp
- HashMap: Tìm kiếm key nhanh O(1)
- TreeMap: Tìm kiếm key O(log n), key tự sắp xếp

## Tiếp theo: [Bài 12: Override và Overload trong Java](/MyPortfolio/p/bai-12-override-overload/)
