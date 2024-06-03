---
title: MarkDown 문법 총정리
author: Hyeonsuk
date: 2024-06-02
category: Jekyll
layout: post
---

## 1. Headers

```markdown
> ###### H6 
> ##### H5
> #### H4
> ### H3
> ## H2  or ---
> # H1 or ===
```



| Markdown | Html |Description |
| -------- | ---- |----------- |
| Header1   |   <h1>heading level 1</h1>   | <span class="h1"> H1 </span>  |
| Header2   |   <h2>heading level 2</h2>   | <span class="h2"> H1 </span>  |
| Header3   |   <h3>heading level 3</h3>   | <span class="h3"> H1 </span>  |
| Header4   |   <h4>heading level 4</h4>   | <span class="h4"> H1 </span>  |
| Header5   |   <h5>heading level 5</h5>   | <span class="h5"> H1 </span>  |
| Header6   |   <h6>heading level 6</h6>   | <span class="h6"> H1 </span>  |



## 2. Block Quote

```markdown
> This is a first blockqute.
>> This is a second blockqute.
>>> This is a third blockqute.
```
> This is a first blockqute.
>> This is a second blockqute.
>>> This is a third blockqute.

다른 마크다운 요소도 포함 가능
> This is h1
> * This is 
> ```code```


## 3. Emphasis

### 3.1 Bold

```markdown
I Just love**bold**
I Just love __bold__
Love **is** bold
```

| Markdown | Html |Description |
| -------- | ---- |----------- |
| ```I Just love **bold**``` | ```I Just love <strong>bold</strong>``` | I Just love **bold** |
| ```I Just love __bold__``` | ```I Just love <strong>bold</strong>``` | I Just love __bold__ |
| ```Love**is**bold``` |   ```I Just love <strong>bold</strong>``` | Love**is**bold |


### 3.2 Italic

```markdown
I Just love*bold*
I Just love _bold_
Love *is* bold
```

| Markdown | Html |Description |
| -------- | ---- |----------- |
| ```I Just love *bold*``` | ```I Just love <em>bold</em>``` | I Just love *bold* |
| ```I Just love _bold_``` | ```I Just love <em>bold</em>``` | I Just love _bold_ |
| ```Love*is*bold``` |   ```I Just love <em>bold</em>``` | Love*is*bold |