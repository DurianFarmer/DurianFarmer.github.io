---
layout: index
title: Test Page
permalink: /test/
sidebar_link: true
sidebar_sort_order: 1
---
# Test Page

**사람은 무엇으로 사는가?**  
$$e^{i} + 1 = 0$$

 ## Static Page (not post) 만드는 법
 * `./`에 `page이름.md`으로 페이지를 만든다.
 * front-matter를 다음과 같이 작성 *(cf. `includes\`)*
 
 ```
 ---
layout: index # page나 default로 하면 .md를 인식 못함 -----
title: Test Page # sidebar에 표시되는 이름
permalink: /test/ # url
sidebar_link: true # 사이드바에 제목 넣기
sidebar_sort_order: 1 # 사이드바 배치 순서
---
 ```

