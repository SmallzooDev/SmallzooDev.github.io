# Vimwiki + Jekyll + Github.io

- vimwiki를 통해 obsidian과 블로그를 대체 할 수 있다는 생각에 열심히 뚝딱뚝딱 만드는 중 입니다.
- https://github.com/SmallzooDev/nvimConfig 이 레포와 같이 작업중입니다.
- 개인적인 고민들이 많은데, 글로 잘 담아보고싶습니다

## 글 작성하기

### 새로운 카테고리 만들기

카테고리가 있는 글을 작성하고 싶을 때는 카테고리를 먼저 만들어야 합니다.
`/_wiki/category-name.md`같이 파일을 만들고 내용에는 다음을 추가해야 합니다.  

이때 `layout`속성은 `category`가 되어야 합니다.

```markdown
---
layout  : category
title   : 제목을 입력합니다.
summary : 
date    : 2022-10-06 00:00:00 +0900
updated : 2022-10-06 00:00:00 +0900
tag     : 
toc     : true
public  : true
parent  : index
latex   : false
---

* TOC
{:toc}
```

### 위키에 글 등록하기

위키를 작성할 때는 `/_wiki` 폴더 아래에 마크다운으로 파일을 작성합니다. 만약
카테고리 아래에 글을 작성하고 싶을 경우에는 카테고리 이름으로 폴더를 만들고
파일을 추가합니다. 예를 들어 `/_wiki/category-name/document.md`로 만들 수 있습니다.
`layout`은 `wiki`가 되어야 합니다. `parent`는 상위 카테고리 이름을 작성해야
합니다.  

만약 상위 카테고리가 없을 경우에는 `parent`에 `index`를 입력합니다.

```markdown
---
layout  : wiki
title   : 제목을 적습니다
date    : 2022-10-08 11:23:00 +0900
updated : 2022-10-08 11:23:00 +0900
tag     : 
toc     : true
public  : true
parent  : category-name
latex   : false
---

* TOC
{:toc}

내용을 적습니다.
```
