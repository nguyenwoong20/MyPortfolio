---
title: "Bài 5 - Câu điều kiện (if-else) và Vòng lặp trong Java"
slug: "bai-5-control-flow"
date: 2025-09-22T11:00:00+07:00
categories: ["Java Series", "Java Cơ Bản"]
tags: ["java-basic"]
series: ["Java Basic"]
series_order: 5
draft: false
image: "https://img.youtube.com/vi/u4kJ-pUKaiQ/maxresdefault.jpg"
---

## 🎥 Video minh họa nguồn: YTB Code Thu
{{< youtube u4kJ-pUKaiQ >}}

---

## 1) Câu lệnh điều kiện if-else
Dùng để kiểm tra điều kiện, phân nhánh logic chương trình.

```java
int age = 19;
if (age >= 18) {
    System.out.println("Bạn đủ tuổi!");
} else {
    System.out.println("Bạn chưa đủ tuổi.");
}
```

## 2) Vòng lặp While
Dùng lặp khi chưa biết trước số lần lặp, lặp khi điều kiện còn đúng.

```java
int i = 0;
while (i < 5) {
    System.out.println("i = " + i);
    i++;
}
```

## 3) Vòng lặp For
Dùng lặp biết trước số lần, cấu trúc gồm khởi tạo, điều kiện, bước nhảy.

```java
for (int j = 1; j <= 3; j++) {
    System.out.println("j = " + j);
}
```

## 4) Kết hợp điều kiện và vòng lặp
Ứng dụng kiểm tra số chẵn/lẻ, tổng dãy số, lọc dữ liệu, ...

```java
for (int k = 0; k < 10; k++) {
    if (k % 2 == 0) {
        System.out.println(k + " là số chẵn");
    }
}
```

## 5) Lời khuyên & cảm nhận
- Nhờ video Code Thủ, mình hiểu rõ từng loại vòng lặp, điều kiện và biết áp dụng chọn đúng tình huống giúp mã nguồn ngắn gọn, hiệu quả.

- Khi học thao tác vòng lặp, đừng quên điều kiện dừng để tránh lỗi infinite loop!

## Tiếp theo: [Bài 6 – Mảng & ArrayList](/MyPortfolio/p/bai-6-array-arraylist/)
