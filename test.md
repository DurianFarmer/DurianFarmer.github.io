---
layout: page
title: Test Page
permalink: /test/
use_math: true
sidebar_link: true
sidebar_sort_order: 1
---

***사람은 무엇으로 사는가?***  

$$ e^{i \pi} + 1 = 0 $$

## Static Page (not Post) 만드는 법
- `./`에 `page이름.md`으로 페이지를 만든다.
- front-matter를 다음과 같이 작성

```
---
layout: page
title: Test Page # sidebar 및 Page 최상단에 표시되는 제목
use_math: true #use_math가 true인 page/post만 LaTex 수식 표현 사용 가능. 다른 곳에서는 $ 표시가 그대로 나타남.
permalink: /test/ # Page의 url
sidebar_link: true # 사이드바에 title 표시. "_includes\page_links.html" 및 "README.md" 참고
sidebar_sort_order: 1 # 사이드바 title 배치 순서
---
```

## 수식 넣는 법
- `_layouts\default.html`에 **MathJax v3**와 연동하는 html 태그 추가하였음.

```html       
  <script>
    MathJax = {
      tex: {
        inlineMath: [ ['$', '$'], ['\\(', '\\)'] ]
      },
      svg: {
        fontCache: 'global'
      }
    };
  </script>
  
  <script type="text/javascript" id="MathJax-script" 
  async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js"></script>
```
- **첫번째 script**
  - in-line 수식을 `$ 수식 $` 식으로 쓸 수 있게 해줌.
  - else, `\\( 수식 \\)` 같은 형태로 써야함. 
  - \$는 달러 기호로 다른 많은 곳에 쓰이므로, front-matter에 `use_math: true`를 설정한 문서만 `$ 수식 $` 표현 가능하도록 함.
  - front-matter에 `use_math: true`를 설정한 문서에서 \$ 기호를 쓰고 싶은 경우: `\$`로 타이핑.
- **두번째 script:** Jekyll과 MathJax v3를 연동하여 LaTex 수식 쓸 수 있게 해줌
- 참고: [Jekyll MathJax v3 연동 및 in-line 수식 \$ 표시로](https://www.bodunhu.com/blog/posts/add-mathjax-v3-support-to-jekyll-and-hugo/)
- 수식이 잘 써지는지 테스트: \\(F=ma\\), $V = IR$

