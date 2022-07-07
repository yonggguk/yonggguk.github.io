---
title: Github 블로그 생성하기 ver.0.0.1
author: yonggguk
date: 2022-07-04 09:00 +0900
categories: [GithubBlog]
tags: [Guide]
mermaid: true
---

chirpy가 아닌 다른 테마 또는 직접 코드를 작성하여 깃허브 블로그를 사용하실 분에게는 참고만 하시거나 다른 글을 찾아보시길 바랍니다.

## Base Settings

ruby가 필요하므로 ruby를 설치하시길 바랍니다

reference : [ruby install docs](https://www.ruby-lang.org/ko/documentation/installation/#rubyinstaller)

## chripy theme 적용

1. chirpy를 통해 직접 설치
2. github에서 fork 받아서 만들기
3. zip file download를 통해 설치하기

저는 3번째 방법을 사용했기에 이 글에서는 3번째 방법만 다룰 예정입니다.

github page repo를 생성했다는 가정 하에 진행하겠습니다!.

### chirpy theme zip파일 다운받기

1. [chripy theme](https://github.com/cotes2020/jekyll-theme-chirpy) 옆 chripy theme github에서 chripy theme 코드 파일을 받은 후 github page local repo에 올려주시면 되겠습니다.

2. local repo에 올린 후 remote repo로 commit을 해주세요. (주의, commit 시 .gitignore에 Gemfile.lock을 추가 후 넣어 주시길 바라겠습니다.)

3. commit후 git bash 또는 powerShell을 통해 설정을 합시다.

### chirpy theme 설정

(1) git bash 또는 powerShell을 통해 bash tools/init.sh 명령어로 기초 설정을 하겠습니다.

(2) 이후 아래 명령어를 통해 Dependencies 설치를 해줍시다.
  
    $ bundle
  
(3) 로컬 서버로 적용된 테마가 잘 동작하는지 확인해 보겠습니다.

    $ bundle exec jekyll s

### remote git-page repo 설정

(1) chripy theme 설정에서 ```bash tools/init.sh``` 명령어를 실행한 이후 local repo의 remote repo와 상태가 다를 겁니다. 상태가 다르니 커밋을 해주어 상태를 맞춰 줍시다.

(2) remote repo와 local repo의 상태가 같다면 remote repo에서 action을 통해 빌드가 잘 되었는지 확인해봅시다.

(3) 빌드가 잘 되었다면, ```https://username/github.io``` 로 접속하여 확인해봅시다.

reference blog : https://www.irgroup.org/posts/jekyll-chirpy/

이상한 용어 혹은 잘못된 표현이 있을 경우 메일이나 github에 이슈로 피드백 남겨주시면 감사하겠습니다. ^__^
![google-analytics-realtime](/posts/20210103/02-google-analytics-realtime.png){: width="616" height="557"}