---
title: Ubuntu Screen Permission 문제 해결
date: 2023-01-07 12:30:00 -0500
author: kintiru
categories: [Korean, Development]   # [TOP_CATEGORIE, SUB_CATEGORIE]
tags: [Korean]     # TAG names should always be lowercase
math: true
---

WSL 2 Ubuntu Distribution에서 screen을 사용하려고 하는데 아래와 같은 에러가 떴다.

``` console
Cannot make directory '/run/screen': Permission denied
```

해결법은 간단하다.

``` sh
sudo /etc/init.d/screen-cleanup start
```
이 명령어를 실행해주면 된다. 


혹은 다음과 같은 상황이라면 이렇게 해결할 수 있다.

``` console
$ systemctl is-enabled screen-cleanup.service

masked

$ file /lib/systemd/system/screen-cleanup.service

/lib/systemd/system/screen-cleanup.service: symbolic link to /dev/null
```

아래 명령어를 이용해서 심볼릭 링크를 지우고 다시 서비스를 설정한다.

``` sh
rm /lib/systemd/system/screen-cleanup.service

systemctl enable screen-cleanup.service

systemctl start screen-cleanup.service
```
