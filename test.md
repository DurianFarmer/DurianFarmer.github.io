---
layout: page
title: Test Page
permalink: /test/
sidebar_link: true
sidebar_sort_order: 1
---

***사람은 무엇으로 사는가?***
$$e^{i} + 1 = 0$$

 ## Static Page (not Post) 만드는 법
 * `./`에 `page이름.md`으로 페이지를 만든다.
 * front-matter를 다음과 같이 작성 *(cf. `includes\page_links.html` 참고)*
 
 ```
 ---
layout: page
title: Test Page # sidebar 및 Page 최상단에 표시되는 이름
permalink: /test/ # Page의 url
use_math: true # mathjax 이용한 수식 표현 가능해짐
sidebar_link: true # 사이드바에 표시하기(제목은 title과 동일함)
sidebar_sort_order: 1 # 사이드바 배치 순서
---
 ```

