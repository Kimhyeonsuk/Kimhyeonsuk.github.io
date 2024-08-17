---
title: Static Export를 위한 시행착오
author: Hyeonsuk
date: 2024-08-15
category: Jekyll
layout: post
---

### Outline
이 포스트는 Server rendering을 위해 구현된 project를 `static export`하기 위해 작성한 포스트이다.~~사실 Chrome extension을 만들기 위해~~

사용한 프로젝트는 next.js showcase에 있는 AI Chatbot template을 이용했다.
해당 프로젝틑 Server rendering을 통해 구현되어 있으며, 프로젝트를 뜯어보면서 Static export를 할 수 있도록 변경하고, 해당 export된 프로젝트를 chrome extension으로 등록하려 하기 위함이다.

App router로 구현하려고 한다.

### Folder structure
* Top lelvel folder는 아래와 같이 분류된다.
    * app
    * src
    * public
* component folder와 lib 폴더는??
    * `/components` 와 `/lib`폴더도 src 아래에 넣어준다.
    * [참고][1]

* nextja-chat -> whale 로 이전
    * `src`폴더 아래에 `/lib` 폴더와 `/components` 폴더를 이전
    * package.json dependency를 복사.


    ![Alt text](image-1.png)


    * prettier.config.cjs 파일 복사

### Remove Auth
* 난 auth관련 내용은 사용하지 않을 것이기 때문에 auth와 관련된 코드를 제거할 것 이다.
![Alt text](image-2.png)

* Index page에서 아래와 같이 auth method를 통해 사용자의 정보를 받아오고 있다.
```
  const session = (await auth()) as Session

```
* Session 정보
```
export interface Session {
  user: {
    id: string
    email: string
  }
}
```
* auth.ts 파일을 생성 후, 아래와 같이 const value를 리턴하도록 해주었다.
```
export const auth = () => {
    return {
        user: {
            id: 'sukrrard',
            email: 'sukrard97@gmail.com'
        }
    }
}
```
* 해당 함수는 단순 const return이므로 await auth()라고 작성된 함수를 모두 바꾸어 주엇다.
![Alt text](image-3.png)

### Build
* 빌드 성공한 모습.
![Alt text](image-4.png)

### Static Export
* 이제 static export를 통해 Chrome extension에 등록하기 위한 `out`폴더를 생성해보도록 하려고 한다.
* next.config.mjs에 아래와 같이 `output: 'export'`를 추가해서 `pnpm build` 명령어를 수행해 보자

* 역시 build 실패, signIn, singUp, Login 관련 코드를 모두 삭제해보자


### Supported Features
* Dynamic Routes when using `getStaticPath`

[1]: https://nextjs.org/docs/app/building-your-application/configuring/src-directory