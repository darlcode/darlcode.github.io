---
layout: post
title: "Java 컴파일"
author: "Bananag"
tags: Java
---

# Java

### 1. Java 컴파일 명령어

```
// 기본 컴파일
$javac 파일명.java

// 클래스파일의 위치를 지정하여 컴파일
// -d 옵션으로 폴더 위치를 지정
$javac -d 클래스파일위치 파일명.java

// 외부라이브러리를 import하여 컴파일
// -classpath 또는 -cp 옵션이용
$javac -cp import하는_외부_라이브러리 파일명.java
$javac -cp "import하는_외부_라이브러리" 파일명.java
```

