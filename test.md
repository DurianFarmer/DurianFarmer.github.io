---
layout: page
title: Test Page
permalink: /test/
use_math: true
sidebar_link: true
sidebar_sort_order: 1
---

***사람은 무엇으로 사는가?***  

$$ e^{i} + 1 = 0 $$

## Static Page (not Post) 만드는 법
- `./`에 `page이름.md`으로 페이지를 만든다.
- front-matter를 다음과 같이 작성 *(cf. `includes\page_links.html` 참고)*
 
```
---
layout: page
title: Test Page # sidebar 및 Page 최상단에 표시되는 이름
use_math: true #use_math를 사용하는 page/post만 latex 표현 사용. else, $는 달러로 표시.
permalink: /test/ # Page의 url
sidebar_link: true # 사이드바에 표시하기(제목은 title과 동일함)
sidebar_sort_order: 1 # 사이드바 배치 순서
---
```

## 수식 넣는 법
- `_layouts\default.html`에 아래 html 태그 추가.
```html       
  <script type="text/javascript" id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js"></script>
```
- 참고: [https://blog.studia.blue/web/jekyll-mathjax/](https://blog.studia.blue/web/jekyll-mathjax/)
- 수식이 잘 써지는지 테스트: \\( F=ma \\)
- inline 수식은 $ 대신 `\\( 수식 \\)` 꼴로 써야 함. $가 너무 흔히 쓰이는 표현이기 때문임.
- block 수식은 $ 두 개 쓰는 통상 노테이션 이용하면 됨.


