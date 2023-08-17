---
layout: post
title: Connect Github Homepage with Domain Name
categories:  
  - gitblog
tags:
  - gitblog
---

___

## 도메인 용어 설명
- **최상위 도메인 (apex domain):** kyuwookchai.com (즉, www. 등이 붙지 않은 도메인이 내 최상위 도메인임)

- **Sub 도메인 (sub domain):** www.kyuwookchai.com, m.kyuwookcahi.com 등

___

## Github homepage에 내 도메인 (GoDaddy에서 구입) 연결하기
1. 링크의 **"Configuring a subdomain"** 프로세스를 수행: [(링크)](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)

	- 과정 1.을 완료하면, 사용자가 www.kyuwookchai.com 이라고 입력했을 때 durianfarmer.github.io 로 포워드 됨.
	- 이제 사용자가 kyuwookchai.com이라고 입력했을 때 www.kyuwookchai.com 으로 포워드해주는 작업을 해주면 됨.
	
2. GoDaddy에서 "전달(하단에 있음)" 기능 설정<br>
*cf. 전달 기능:  사용자가 내 최상위 도메인(kyuwookchai.com)을 입력했을 때 다른 도메인(내 Sub 도메인(www.kyuwookchai.com) 포함)으로 포워드하는 기능.*
	
    - **여기로 전달 (사용자가 kyuwookchai.com 을 입력했을 때 어디로 포워드할지 설정하는 창임):** <br>
        https:/ <br>
        www.kyuwookchai.com <br>
		
    - **전달유형:** 영구
    - **설정:** 포워딩만 가능