---
title: 구현
author: Hyeonsuk
date: 2024-08-08
category: Jekyll
layout: post
---

## Project 초기 구성
npm build package는 yarn을 이용하여 구성하였다.
`npm create-react-app`을 통해서는 chrome extension을 구성하기 어렵다는 말이 있어 `webpack`을 통해 구성하려고 한다.
[관련 링크][1]

`yarn init -y`

## 의존성 설치

```yarn add -D webpack webpack-cli ```
* webpack은 코드와 선택적으로 모든 의존성을 하나의 .js로 묶는 도구


```
yarn add -D react react-dom
yarn add -D @types/react @types/react-dom 
```

* @types/ 접두사는 React와 React-DOM의 선언 파일을 가져오고 싶다는 것을 의미함. 일반적으로 "react"와 같은 경로를 가져오면, react 패키지 자체를 살펴볼 것입니다; 그러나 모든 패키지에 선언 파일이 포함되어 있지 않기 때문에, TypeScript는 @types/react 패키지도 찾습니다. 나중에는 이것에 대해 생각할 필요가 없다는 것을 알 수 있습니다.




[1]: https://typescript-kr.github.io/pages/tutorials/react-&-webpack.html
