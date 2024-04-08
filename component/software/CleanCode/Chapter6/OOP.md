---
title: 객체와 자료구조
author: Hyeonsuk
date: 2024-04-08
category: Jekyll
layout: post
---


### 자료 추상화

#### 구체적인 Point Class
```java
public class Point{
    public double x;
    public double y;
}
```

#### 추상적인 Point Class
```java
public class Point{
    double getX();
    double getY();
    void setCartesian(double x, double y);
    double getR();
    double getTheta();
    void setPolar(double r, double theta);
}
```

- 두번째 클래스는 접근 정첵을 강제
- 사용자가 구현을 모른 채, 자료의 핵심을 조작.


#### 구체적인 vehicle 클래스
```java
public interface Vehicle{
    double getFuelTankCapacityInGallons();
    double getGallonsOfGasoline();
}
```

#### 추상적인 Vehicle 클래스
```java
public interface Vehicle{
    double getPercentFuelRemaining();
}
```
