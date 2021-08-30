---
title:  "[C++] 함수 리턴 타입 추론"
excerpt: "함수 리턴 타입 추론에 사용되는 auto 키워드"
toc: true
toc_sticky: true

categories:
  - C++
tags:
  - C++
last_modified_at: 2021-08-30T22:15:00
---

* 참고문헌 : 전문가를 위한 C++(마크 그레고리 / 한빛미디어)

`C++14`부터 함수의 리턴 타입을 컴파일러가 알아서 지정하도록 하는 `auto`키워드를 사용할 수 있음.

```cpp
auto addNumbers(int number1, int number2)
{
  return number1 + number2;
}
```

* 컴파일러는 `return`문에 나온 표현식의 타입에 따라 리턴 타입을 추론함.
* 함수 내에 여러 개의 `return` 문이 있는 경우, 각 타입은 모두 같아야 함.
