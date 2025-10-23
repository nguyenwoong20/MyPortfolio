---
title: "Bài 1 - Giới thiệu Java & môi trường lập trình (Hello World)"
date: 2025-09-22T09:00:00+07:00
categories: ["Java Series", "Java Cơ Bản"]
tags: ["java-basic"]
series: ["Java Basic"]
series_order: 1
draft: false
image: "https://img.youtube.com/vi/uWdaOoMgFvs/maxresdefault.jpg"
---

## 🎥 Video minh họa nguồn: YTB Code Thu
{{< youtube uWdaOoMgFvs>}}

---

## 1) Chuẩn bị môi trường Java
- Tải về **JDK** (khuyên dùng Temurin hoặc Oracle JDK).  

- Cài đặt xong, kiểm tra trên terminal/cmd:

```bash
java -version
javac -version
```
Thiết lập biến môi trường JAVA_HOME nếu cần cho dự án/IDE.

## 2) Cài đặt IDE chuyên dụng
- IntelliJ IDEA Community Edition (Code Thủ hướng dẫn thao tác siêu nhanh)

- Hoặc VS Code (cài Java Extension Pack)

- IDE miễn phí, dễ thao tác cho người mới.

## 3) Tạo Project & file đầu tiên (Hello World)
- Trong IntelliJ: File > New > Project, chọn Java, rồi tạo file Hello.java trong thư mục src.

- Cấu trúc dự án đơn giản:

```bash
ProjectRoot/
└── src/
    └── Hello.java
```
## 4) Viết chương trình đầu tiên

```bash
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello, Java!");
    }
}
```
- Build và chạy bằng nút Run trên IDE, hoặc dùng dòng lệnh:

```bash
javac Hello.java
java Hello
```
- Màn hình in ra:

```bash
Hello, Java!
```
## 5) Kết luận & cảm nhận
- Sau khi xem video của Code Thủ, mình cài đặt Java, thiết lập IDE và chạy chương trình đầu tiên cực kỳ nhanh, y như hướng dẫn!

- Việc xây dựng dự án Java và chạy mã nguồn đơn giản giúp mình tự tin bắt đầu học các phần tiếp theo.

## 📚 Bài tiếp theo
👉 [**Bài 2 – Boolean – Cái Đúng Cái Sai trong Java**](/MyPortfolio/p/bai-2-boolean-cai-dung-cai-sai-trong-java/)
