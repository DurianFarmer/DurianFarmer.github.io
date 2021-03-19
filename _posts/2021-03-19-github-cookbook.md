---
layout: post
title: Github Cookbook
categories:
  - github
tags:
  - github
---

 ### github -> local
 | Code | Memo |
 | --- | --- |
 | `git init`<br>`git remote add origin https://github.com/DurianFarmer/stocks_kr.git` | local이 github과 연동되도록 설정 <br> 내가 처음 프로젝트를 만들었을 때 사용 |
 | `git pull origin master` | github -> local로 프로젝트를 가져오기 |
 | `git clone https://github.com/DurianFarmer/stocks_kr.git` | github에 이미 올라와 있는 project를 local로 그대로 가져오기 <br> 주로 다른 사람이 만든 프로젝트를 가져올 때 사용 |

### local -> github
| Code | Memo 
| --- | --- 
| `git status` | local과 github의 차이 보여주기
| `git add .` | 모든 차이를 track하겠음
| `git commit -m 210319` | track한 내용을 확정
| `git push origin master` | local -> github

### miscellaneous
| Code | Memo |
| --- | --- | 
| `git config --global core.autocrlf true` | 이 기능은 개발자가 git에 코드를 추가했을 때 (예컨대 커밋할 때)에는 CRLF를 LF로 변환해주고, git의 코드를 개발자가 조회할 때 (예컨대 clone한다거나 할 때)에는 LF를 CRLF로 변환해준다. <br> 그러므로 윈도우 사용자의 경우 이러한 변환이 항상 실행되도록 다음과 같은 명령어를 입력한다. 물론 시스템 전체가 아닌 해당 프로젝트에만 적용하고 싶다면 —global 을 빼주면 된다. |
| `git config --global core.autocrlf true input` | 리눅스나 맥을 사용하고 있는 경우, 조회할 때 LF를 CRLF를 변환하는 것은 원하지 않을 것이다. 따라서 뒤에 input이라는 명령어를 추가해줌으로써 단방향으로만 변환이 이루어지도록 설정한다. |