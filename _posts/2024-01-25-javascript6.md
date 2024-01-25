---
title: javascript_6
date: 2024-01-25 23:00:00 +0900
categories: [javascript]
tags: [js]
---

### 🌟 String

* 백틱 ``
    ```javascript
    let desc =`오늘은 맑고 
    날씨가 계속되겠습니다.`;    //백틱 줄바꿈 가능

    let desc ='오늘은 맑고\n날씨가 계속되겠습니다.';
    ```

* [] 배열처럼 문자열 위치 접근 가능
  ```javascript
  let desc ='안녕하세요.';
  desc[2]; //하
  desc[4] = "용"; //변화 없음
  ```

* isNaN() : NaN을 판단할 수 있는 유일한 함수
  ```javascript
    let x = Number('x');  //NaN

    x == NaN //false
    x === NaN //false
    NaN == NaN //false
    
    isNaN(x)  //true
    isNaN(3)  //false
  ```

* indexOf(text)
  ```javascript
   let desc = "Hello, Everyone!";
   desc.indexOf('of');  //-1

   //주의
   if(desc.indexOf("Hello") > -1){  //0으로 시작하므로 false -1로 비교해야함
    console.log("Hello가 포함된 문장");
   }

  ```

* slice(n, m)
  + n : 시작점 
  + m : 없으면 문자열 끝 / 양수면 그 숫자까지(포함X) / 음수면 끝에서부터
  ```javascript
    let desc ="abcdefg";
    desc.slice(2, -2); //cde //끝에서 2번째
  ```

* substring(n, m)
  + n 과 m 사이
  + n 과 m 바꿔도 동일하게 동작
  + 음수 불가
   
* substr(n, m)
  + n부터 시작하여 m개 가져옴

<br><br><br><br>

:star: 코딩애플's [자바스크립트 중급 강좌](https://www.youtube.com/watch?v=G360D6lqrfo&list=PLZKTXPmaJk8JZ2NAC538UzhY_UNqMdZB4&index=6)를 보고 정리한 것입니다.