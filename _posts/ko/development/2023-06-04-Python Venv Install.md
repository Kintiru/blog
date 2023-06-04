---
title: '파이썬 venv 설치하기'
date: 2023-04-04 11:00:00 +0900
author: kintiru
categories: [Korean, Development]   # [TOP_CATEGORIE, SUB_CATEGORIE]
tags: [Korean]     # TAG names should always be lowercase
math: true
mermaid: true
#img_path: 
#image: #preview image
    #path:
    #alt:
    #lqpq:
#pin: true
---

## 원하는 버전의 파이썬 설치하기

```{bash}
sudo add-apt-repository -y ppa:deadsnakes/ppa
sudo apt update
sudo apt install -y python3.10
sudo apt install -y python3.10-venv
sudo apt install -y python3.10-dev
```

해당 글에서는 파이썬 3.10 버전을 기준으로 작성하도록 하겠다.

만약에 3.11을 설치하고 싶다면 `python3.10`을 `python3.11`로 수정해주면 된다.
이 글에서 설명하는 모든 것에 똑같이 원하는 버전으로 변경해주면 된다.

## Venv

```{bash}
python3.10 -m venv /path/to/folder
```
`/path/to/folder`는 원하는 경로로 설정해주면 된다.

해당 명령어를 입력하면 입력한 경로에 venv환경이 생성된다.

```{bash}
cd /path/to/folder
source bin/activate
```
cd 대신에 그냥 아예 `source /path/to/folder/bin/activate`를 사용해도 무관하다.