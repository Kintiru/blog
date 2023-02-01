---
title: 'How to change KaTeX Font and Color'
date: 2020-10-04 00:00:00 +0900
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

블로그를 세팅하면서 여러가지 KaTeX관련 문제가 있었는데,

KaTeX가 어두운 테마에서도 글자 색상이 동일해서 안 보이는 문제와

모바일에서 화면 밖으로 나가는 문제가 있었다.

폰트도 마음에 안 들어서 같이 설정을 바꾸어주었다.

아래와 같은 방 식으로 .katex 안에 properties를 지정해주면 된다.

```css
.katex { 
        font: 1em "your-font", font-family !important;
        color: white;
        overflow: auto;
    }
```