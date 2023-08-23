---
layout: post
title: Static Page in Gitblog
categories:  
  - gitblog
tags:
  - gitblog
---

## Static Page (not Post) 만드는 법
- `./`에 `page이름.md`으로 마크다운 파일을 만든다.
- front-matter를 다음과 같이 작성

```
---
layout: page # post가 아닌 page임
title: Test Page # sidebar 및 Page 최상단에 표시되는 제목
use_math: true #use_math가 true인 page/post만 LaTex 수식 표현 사용 가능. 다른 곳에서는 $ 표시가 그대로 나타남.
permalink: /test/ # Page의 url. 예: kyuwookchai.com/test
sidebar_link: true # 사이드바에 title 표시. "_includes\page_links.html" 및 "README.md" 참고
sidebar_sort_order: 1 # 사이드바 title 배치 순서
---
```

- 이후에는 마크다운으로 페이지 컨텐츠 작성하면 됨.
- Title은 `heading2(##)`부터 사용. front-matter 통해 설정하는 제목이 `heading1 (#)`이 되기 때문임.