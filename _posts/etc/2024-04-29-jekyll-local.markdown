---
layout: post
title: jekyll 로컬에서 돌리기 성공
date: 2024-04-29 14:35:00 +0900
category: Etc.
---
세번의 시도 끝에 성공했다.

전체적인 과정은 사실 간단하다.
1. 루비 설치
2. 프로젝트로 이동
3. 서버 실행

아래로는 더 자세한 과정을 풀어보겠다.

---
[Ruby](https://rubyinstaller.org/)  

해당 링크에서 원하는 버전의 루비를 다운받는다.

![img.png](/public/img/etc/img.png)  
1번 또는 3번을 입력해 다운 받는다. (나는 3번을 입력했다.)  

![img.png](/public/img/etc/img_1.png)  
다운로드 완료 후 위의 프로그램 실행  
```
gem install jekyll bundle
```
블로그 프로젝트를 미리 클론 해놨었기 떄문에 해당 위치로 이동만 했다.
```
cd [유저이름.github.io 저장 위치]

bundle exec jekyll serve
```
성공.  
http://127.0.0.1:4000/ 로 접속하면 로컬로 확인하며 수정할 수 있다.

---
'bundle install' 을 찾을 수 없는 오류
계속되는 오류에 모두 삭제하고 다시 시도했을 때 뜬 오류이다.
해결 법은 손상된 파일인 .bundle/config 를 삭제 한 후 다시 다운 받는 것.
```
rm .bindle/config

gem update --system

gem update bundler

bundler install
```
폴더 위치를 유념하자. 아무 생각없이 github.io 폴더 안에서 실행하고 허겁지겁 뇌에 힘줬다.