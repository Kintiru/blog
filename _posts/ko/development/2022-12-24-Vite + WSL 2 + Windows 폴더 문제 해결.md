---
title: Vite + WSL2 + Windows 폴더 문제 해결
date: 2022-12-24 10:02:00 +0900
author: kintiru
categories: [Korean, Development]   # [TOP_CATEGORIE, SUB_CATEGORIE]
tags: [Korean, React, Typescript]     # TAG names should always be lowercase
math: true
---

최근에 WSL2 를 사용해서 리액트 개발환경을 구축하는데, 프로젝트 폴더가 윈도우 파일시스템 안에 있으면 제대로 HMR Update를 못하는 이슈가 발생했다.

이 이슈는 이미 Vite 공식 문서에도 나와있는 해결방법이지만, 메모도 할겸 두가지 예시를 포스팅하려고 한다.

## 방법

`server.watch` 안에 `{ usePolling: true }` 를 추가해주면 된다.

## 예시

```typescript
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'

// https://vitejs.dev/config/
export default defineConfig({
  plugins: [react()],
  server: {
    watch: {
      usePolling: true,
    }
  }
})
```
