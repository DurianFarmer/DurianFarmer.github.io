---
layout: post
title: Using Equations in Gitblog
use_math: true
categories:  
  - gitblog
tags:
  - gitblog
---

## Great

$$ e^{i \pi} + 1 = 0 $$

## 수식 넣는 법
- `_layouts\post.html`, `_layouts\page.html` 각각에 **MathJax v3**와 연동하는 html `<script>` 태그 두 개를 추가하였음.
- ***cf. 둘의 상위인 `_layouts\default.html`에 `<script>` 태그를 넣으면 Post 생성 시 수식 적용 안 됨.

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