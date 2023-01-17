---
title: 'Chirpy Jekyll 블로그 Github Page로 설치하기'
date: 2023-01-09 13:55:00 +0900
author: kintiru
categories: [Korean, Daily]   # [TOP_CATEGORIE, SUB_CATEGORIE]
tags: [Korean, Daily]     # TAG names should always be lowercase
math: true
mermaid: true
toc: true
#img_path: 
image: #preview image
    path: https://chirpy-img.netlify.app/commons/devices-mockup.png
    #alt:
    #lqpq:
#pin: true
---
<!--- 
Include script per post to prevent version break and better per post management
-->
<script src="https://cdn.jsdelivr.net/npm/chart.js@4.1.2/dist/chart.umd.js"></script>

기존에 Ghost블로그를 쓰다가 Hashnode로 잠시 넘어갔다가 다시 Ghost를 쓰던 중, 에디터가 너무 불편하고 직접 호스팅 하는 게 조금 불안해져서 Github Page를 이용한 블로그를 만들기로 했다.

옮기게 된 가장 큰 이유는 일단 github은 히스토리가 저장되고, 서버가 다운될 일도 거의 없고, Deploy도 간편하기 때문이다.

# 1. 블로그 테마 clone 하기

![Chirpy Docs](/assets/img/2023/01/2023-01-09%20202949.png)
_Chirpy README 페이지_

여기에 파란색으로 적혀있는 Chirpy Starter를 누르면 새로운 Repository를 만드는 창이 나오는데 거기에 레포 이름을 기입하면 된다.

기본적으로는 `<username>.github.io` 같은 형식으로 만들라고 하지만, 사실 커스텀 도메인을 사용할 예정이라면 어떠한 이름을 써도 상관은 없다.

나의 경우는 커스텀 도메인을 이용했다.

사실, 커스텀 도메인을 안 써도 상관은 없지만 설정이 되게 복잡해지기 때문에 추천하지 않는다.

다만 `<username>.github.io` 같은 형식의 레포 이름이 아니면, `<username>.github.io/<repo name>` 와 같은 url에 생성된다.

여기서 `<username>`이나 `<repo name>`은 직접 설정한 유저명과 레포 이름이다.

# Github Page 설정하기

![Github Page 설정 창](/assets/img/2023/01/2023-01-09%20203626.png)

방금 만든 Repo > Setting에 들어가면 Page라는 옵션이 보일 텐데, 그걸 클릭하면 위와 같은 창이 뜬다. 여기서 Source 아래에 있는 드롭다운을 클릭해서 Github Actions를 선택한다.

여기서 더 아무것도 안 해도 되고, 이제 여기서 그냥 `_config.yml`을 입맛에 맞게 설정해주고 포스트 작성을 시작하면 된다. 

여기서 더 설정을 안 해도 github workflow가 자동으로 설정되어있기 때문에 git push를 하면 자동으로 빌드해서 deploy 해준다.

혹은 Actions 탭에 들어가서 직접 Workflow를 run해주면 deploy 할 수 있다.

# 커스텀 도메인 설정하기 (선택사항)

도메인 설정을 할 수 있는 곳으로 가서 (주로 도메인을 구입한 곳이다), `<subdomain>.example.com` 와 같이 레코드를 설정할 수 있을 것이다. 나의 경우 `<subdomain>`이 page 이고, 이 도메인을 CNAME으로 자기의 깃허브 페이지 주소인 `<username>.github.io` 설정해주면 된다. 

이제 모든 설정이 끝났고, 포스팅을 시작하면 된다.