---
title: Function
author: Hyeonsuk
date: 2024-02-05
category: Jekyll
layout: post
---


### Try/Catch 블록 뽑아내기
- 별도의 함수로 추출해 주는게 코드 가독성에 좋을 것 같다.
- 아래의 예제와 같이 Try catch block 내의 코드를 함수로 추출해주자.

```java
public void delete(Page page){
    try{
        deletePageAndAllReference(page);
    }
    catch (Exception e){
        logError(e);
    }
}
```


