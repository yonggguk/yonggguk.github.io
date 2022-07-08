---
title: Docker 개인 registry 만들기 
author: 1n9yun
date: 2022-02-27 17:48 +0900
categories: [Etc]
tags: [docker]
mermaid: true
---

CI/CD 구축해보다가 필요해지게 되어 개인 Registry를 만들게 되었습니다. 분명히 또 까먹을테고, 또 쓸 일이 있지 않을까 싶어 정리합니다.

## Registry 생성

```
docker run -d -p 5000:5000 \
--name private-registry \
-v {VOLUME}:/var/lib/registry/docker/registry/v2 \
registry
```
`VOLUME`은 이미지를 저장해둘 볼륨을 지정합니다. down되었을 때 날아가면 안되니까요~

## Registry Web (GUI) 

편하게 웹으로 registry를 관리할 수 있습니다

```yml
# config.yml
registry:
 url: http://{REGISTRY_CONTAINER_NAME}:5000/v2
name: {DOMAIN}:{PORT}
```

`docker run`에서 변수로 넘겨주어도되지만.. config파일을 만들어주고  
registry를 일단 로컬에서 사용할 것이므로 `name: localhost:5000`으로 해줬어요

```
docker run -it -d -p 5001:8080 \
--name private-registry-web \
--link private-registry \
-v {CONFIG_PATH}/config.yml:/conf/config.yml:ro \
hyper/docker-registry-web
```
8080 포트는 쓸 일이 많고 괜히 나중에 방해될까봐 5001로 변경해주었어요

끗


![google-analytics-realtime](/posts/20210103/02-google-analytics-realtime.png){: width="616" height="557"}