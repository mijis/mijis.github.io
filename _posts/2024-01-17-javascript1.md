---
title: javascript_1
date: 2024-01-17 22:20:27 +0900
categories: [javascript]
tags: [js]
---

### 1. Javascript's variable

* const, let, var
* 변수 별 특징
  - var : 중복선언 가능 / *선언* 호이스팅 가능
  - let&const : *선언* 호이스팅 가능!  
      ➡ WHY?! __*TDZ*__
   
<br><br>


### 2. Temporal Dead Zone (TDZ) : 일시적 사각지대

* TDZ의 변수들은 사용이 불가능
* 할당 전까지 사용 불가

* error 코드
    ```javascript
    //Error : Uncaught ReferenceError: Cannot access 'age' before initialization
    let age = 30;

    function showAge(){
        console.log(age);
        let age =20;
    }

    showAge();
    ```
    ➡ 호이스팅은 스코프(scope) 단위로 발생 <br>
    ➡ showAge 함수에서 스코프는 함수 내부이므로 함수 시작부터 끝은 TDZ 구간

<br><br>

### 3. 정리
* var
  - 선언 및 초기화(undefined 할당) 단계  
  - 할당 단계
  - 함수 스코프(function-scoped) : var도 함수 내에서 선언되면 벗어날 수 없음

* let : 호이스팅 되면서 선언이 이뤄지지만 초기화는 실제 코드에서 진행
  - 선언 단계
  - 초기화 단계
  - 할당 단계
  - 블록 스코프(block-scoped)

* const
  - 선언 + 초기화 + 할당
    ```javascript
    //에러 코드 (uncaught SyntaxError: Missing initailizer in const declaration)
    const gender;       
    gender = 'male';
    ```
  - 블록 스코프(block-scoped)


<br><br><br><br>

:star: 코딩애플's [자바스크립트 중급 강좌](https://www.youtube.com/watch?v=ocGc-AmWSnQ&list=PLZKTXPmaJk8JZ2NAC538UzhY_UNqMdZB4)를 보고 정리한 것입니다.