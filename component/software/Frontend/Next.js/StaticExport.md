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

### Supported Features
* Dynamic Routes when using `getStaticPath`

[1]: https://nextjs.org/docs/app/building-your-application/configuring/src-directory