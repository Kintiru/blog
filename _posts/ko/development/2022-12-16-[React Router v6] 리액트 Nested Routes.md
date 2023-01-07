---
title: '[React Router v6] 리액트 Nested Routes'
date: 2022-12-16 04:22:00 +0900
author: kintiru
categories: [Korean, Development]   # [TOP_CATEGORIE, SUB_CATEGORIE]
tags: [Korean, React, Typescript]     # TAG names should always be lowercase
math: true
mermaid: true
---
최근에 React 프로젝트에서 React Router를 사용하다가 프로젝트가 생각보다 커져 Route들을 관리하기 쉽도록 Nested Routes를 쓰게 되었다.

리액트를 처음 써보는 프로젝트라서 처음에는 어떻게 해야 하는 지 몰랐고, 현재 느낀 바로는 지금의 React는 기존의 클래스형 컴포넌트에서 함수형 컴포넌트로 넘어가는 도중이고, React Router v6에 관한 글이 별로 없어서 자료를 찾기 힘들었다.

그래서 간단하게 내가 Nested Routes 사용한 방법에 대한 글을 한번 정리해보게 되었다.

## App.js 예시

```typescript
import React from "react";
import { BrowserRouter, Routes, Route } from 'react-router-dom';
import './App.css';
import Home from "./components/Home";
import SubRouter1 from "./components/SubRoute/SubRouter1 ";
import SubRouter2 from "./components/SubRoute/SubRouter2";

export default function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/SubRoute1/*" element={<SubRouter1 />} />
        <Route path="/SubRoute2/*" element={<SubRouter2 />} />
      </Routes>
    </BrowserRouter>
  );
}
```

App.js 는 이런 식으로 작성했다.

각 Path 뒤에 `*` 를 붙임으로써 해당 element 안에 nested rotues를 넣어두었다는 것을 명시한다.

아래에 Nested Route에 대한 예시도 하나 작성해두도록 하겠다.

## SubRouter1.js 예시

```typescript
import React from "react";
import { BrowserRouter, Routes, Route } from 'react-router-dom';

import Component1 from "../dir/Component1";
import Component2 from "../dir/Component2";

const SubRouter1 = () => {
  return (
    <Routes>
      <Route path={"Component1"} element={<Component1 />} />
      <Route path={"Component2"} element={<Component2 />} />
    </Routes>
  );
};

export default SubRouter1;
```

상대경로가 지원 되기 때문에 하위 라우팅 파일에서는 `path="/SubRoute1/Component1"` 대신에 `path="Component"`로 작성해도 제대로 `www.example.com/SubRoute1/Component1`으로 라우팅 된다.