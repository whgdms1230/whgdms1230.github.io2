---
title:  "[C++] uniform initialization"
excerpt: "{...} 문법을 이용한 유니폼 초기화"
toc: true
toc_sticky: true

categories:
  - C++
tags:
  - C++
last_modified_at: 2021-09-09T22:45:00
---

* 참고문헌 : 전문가를 위한 C++(마크 그레고리 / 한빛미디어)

`C++11` 이전에는 구조체나 클래스 등의 타입별로 초기화 방식이 일정하지 않았다. 구조체의 경우 `{...}` 문법을 적용한 반면, 클래스의 경우 `(...)` 문멉을 이용하여 생성자를 호출하였다.

```cpp
ExampleStruct myExample1 = {10, 20}; // 구조체의 초기화
ExampleClass myExample2(10, 20); // 클래스의 초기화
```

`C++11` 부터 타입을 초기화 할 때 `{...}` 문법을 사용하는 유니폼 초기화를 따르도록 통일됐다.

```cpp
ExampleStruct myExample1 = {10, 20}; // 구조체의 초기화
ExampleClass myExample2 = {10, 20}; // 클래스의 초기화
```

또한 등호를 생략해도 된다.

```cpp
ExampleStruct myExample1{10, 20}; // 구조체의 초기화
ExampleClass myExample2{10, 20}; // 클래스의 초기화
```


* 유니폼 이니셜라이저는 구조체나 클래스 뿐만 아니라 C++에 있는 모든 대상을 초기화 하는데 사용된다. 다음의 예시는 네 변수를 모두 3으로 초기화된다.
```cpp
int a = 3;
int b(3);
int c = {3};
int d{3};
```
* 유니폼 초기화는 제로 초기화에도 적용할 수 있다.
```cpp
int e{};
```
* 유니폼 초기화는 동작으로 할당되는 배열을 초기화할 때도 적용할 수 있다.
```cpp
int* pArray = new int[4]{0, 1, 2, 3};
```