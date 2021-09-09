---
title:  "[C++] type inference"
excerpt: "타입 추론의 기본과 auto/decltype"
toc: true
toc_sticky: true

categories:
  - C++
tags:
  - C++
last_modified_at: 2021-09-09T22:15:00
---

* 참고문헌 : 전문가를 위한 C++(마크 그레고리 / 한빛미디어)

타입 추론(`type inference`)는 표현식의 타입을 컴파일러가 스스로 알아내는 기능이다.

## 1. auto

`C++14`부터 함수의 리턴 타입을 컴파일러가 알아서 지정하도록 하는 `auto`키워드를 사용할 수 있음.

다음은 `auto`를 사용하게 되는 상황들이다.

* 함수의 리턴 타입 추론
* 구조적 바인딩에 사용
* 표현식의 타입 추론
* 비타입(`non-type`) 템플릿 매개변수의 타입 추론
* `decltype` (`auto`) 에서 사용
* 함수에 대한 또 다른 문법으로 사용
* 제네릭 람다 표현식에서 사용

다음은 함수의 리턴 타입을 추론에 대한 예시이다.

* 컴파일러는 `return`문에 나온 표현식의 타입에 따라 리턴 타입을 추론함.
* 함수 내에 여러 개의 `return` 문이 있는 경우, 각 타입은 모두 같아야 함.

```cpp
auto addNumbers(int number1, int number2)
{
  return number1 + number2;
}
```

`auto` 키워드는 복잡한 타입에 적용할 때 편리하다. 또한 함수의 리턴 타입을 변경하더라도 코드에서 그 함수가 나온 모든 지점을 고칠 필요 없이 간단히 수정할 수 있다.

하지만 `auto`로 표현식의 타입을 추론하면 **함수에 지정된 레퍼런스나 `const` 한정자가 제거된다.** `const` 레퍼런스 타입으로 지정하려면 auto 키워드 앞뒤에 레퍼런스 타입과 `const` 키워드를 붙여야 한다.

```cpp
const auto& f = foo();
```

## 2. decltype

`decltype` 키워드는 인수로 지정한 표현식의 타입을 알아낸다. 다음 예제는 y의 타입이 x의 타입인 `int` 라고 추론한다.

```cpp
int x = 123;
decltype(x) y = 456;
```

`decltype`은 `auto`와 다르게 레퍼런스나 `const` 키워드를 삭제하지 않는다. 이러한 `decltype`은 템플릿을 사용할 때 효과적이다.