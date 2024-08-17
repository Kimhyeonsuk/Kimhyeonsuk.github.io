---
title: Typescript 기본 문법 정리
author: Hyeonsuk
date: 2024-08-17
category: Jekyll
layout: post
---

### 전개 연산자(Spread Operator)
[doc][1]의 전개연산자에 대한 설명은 다음과 같다.
배열이나 객체의 요소를 `spread` 하기위한 연산자.

전개 연산자는 다음과 같은 세가지 경우에 사용한다.
* 나머지 매개변수를 정의
* 배열 요소를 확장
* 객체 요소를 확장


코드를 통해 보면 다음과 같다.

```
function foo(x, y, z) { }
var args = [0, 1, 2];
foo(...args);
```
```
var [x, y, ...remaining] = [1, 2, 3, 4];
console.log(x, y, remaining); // 1,2,[3,4]
```

#### Object Spread
Spread 연산자는 다음과 같이 다른 object의 요소에 대해서도 `spread`? 할 수 있다.
예제는 다음과 같다.
```
const foo = {a: 1, b: 2, c: 0};
const bar = {c: 1, d: 2};
/** Merge foo and bar */
const fooBar = {...foo, ...bar};
// fooBar is now {a: 1, b: 2, c: 1, d: 2}
```


[1]: https://basarat.gitbook.io/typescript/future-javascript/spread-operator