---
title: "리액트 라우터 개념"
excerpt: "리액트 라우터 v6 개념 소개"

categories:
  - react
tags:
  - React
---

# React Router 개념

리액트 컴포넌트로 페이지를 나누고 이동하게 해주는 라이브러리인 react router에 대해서 소개해 보고자 한다.

### React Router의 핵심 컴포넌트

- Router
  리액트 라우터에서 사용하고 있는 것(현재 주소 등)들을 모두 갖고 있음

  ```
  import {childRouter} from 'react-router-dom';

  function Main() {
    return <childeRouter> ... </childRouter>
  }

  export default Main;
  ```

- Routes & Route
  경로를 찾다가 발견하면 그 안의 컴포넌트 보여줌
  ```
  <Routes>
    <Route path="path" element={<pathListPage />} />
  </Routes>
  </>
  ```
- Link
  리액트 라우터에서 a 태그 대신 사용
