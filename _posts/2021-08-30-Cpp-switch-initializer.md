---
title:  "[C++] switch 문의 이니셜라이저"
excerpt: "switch 문의 이니셜라이저 기능"
toc: true
toc_sticky: true

categories:
  - C++
tags:
  - C++
  - programing
last_modified_at: 2021-08-30T21:48:00
---

if 문과 동일하게 C++17부터 switch 문 안에 이니셜라이저를 넣는 기능이 추가되었음.

```
if (<이니셜라이저> ; <조건문>)
{
  <본문>
}
```

<이니셜라이저>에서 정의한 변수는 <조건문>과 <본문> 안에서만 사용할 수 있고, switch 문 밖에서는 사용할 수 없음.

