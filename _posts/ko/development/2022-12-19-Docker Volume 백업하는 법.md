---
title: Docker Volume 백업하는 법
date: 2022-12-19 07:03:00 +0900
author: kintiru
categories: [Korean, Development]   # [TOP_CATEGORIE, SUB_CATEGORIE]
tags: [Korean]     # TAG names should always be lowercase
math: true
---

이번에 Ghost를 업데이트하면서 혹시 모를 상황에 대비해 Docker Volume을 백업해야하는 상황이 오게 되었다.

``` sh
mkdir ~/backup
docker run --rm --volumes-from <container> -v ~/backup:/backup ubuntu bash -c "cd <path to backup> && tar cvf /backup/backup.tar ."
```

위에 명령어를 이용해서 백업을 진행했다.

이 명령어는 현재 `<container>` 에 연결되어있는 볼륨을 마운트한 더미 도커 컨테이너를 생성하고,\
그 안에서 해당 위치로 이동해서 백업한 다음 컨테이너 밖으로 꺼내고 더미 컨테이너를 지운다.

`<container>` 와 `<path to backup>` 은 백업해야할 볼륨이 연결되어 있는 컨테이너와 그 볼륨 안에서 백업할 위치로 자유롭게 변경하면 된다.

나의 경우 이렇게 사용했다.

``` sh
docker run --rm --volumes-from blog.kintiru.cc -v ~/backup:/backup ubuntu bash -c "cd /var/lib/ghost && tar cvf /backup/ghost.tar ."
```