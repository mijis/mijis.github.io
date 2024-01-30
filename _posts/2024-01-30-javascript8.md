---
title: javascript_7
date: 2024-01-30 23:50:00 +0900
categories: [javascript]
tags: [js]
---

### 🌟 구조 분해 할당

  ```javascript
  let users = ['Mike', 'Tom', 'Jane'];
  let [user1, user2, user3] = users;

  //let user1 = user[0];
  //let user2 = user[1];
  //let user3 = user[2];

  console.log(user1); //Mike
  console.log(user2); //Tom
  console.log(user3); //Jane
  ```

* 배열 구조 분해 : 기본값
  ```javascript
  let [a, b, c] = [1, 2]; //c undefined
  let [a=3, b=4, c=5] = [1, 2]; //기본값 할당 c 5 유지
  ```

* 배열 구조 분해 : 바꿔치기
  ```javascript
  let a = 1;
  let b = 2;

  [a, b] = [b, a];//임시변수를 사용하지 않아도 됨
  ```


<br><br><br><br>

:star: 코딩애플's [자바스크립트 중급 강좌](https://www.youtube.com/watch?v=lV7ulA7R5Nk&list=PLZKTXPmaJk8JZ2NAC538UzhY_UNqMdZB4&index=9)를 보고 정리한 것입니다.