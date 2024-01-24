---
title: javascript_5
date: 2024-01-24 22:17:27 +0900
categories: [javascript]
tags: [js]
---

### 🌟 Math

* toString() : 10진수 다른 진법으로 변환 가능
    ```javascript
    let num = 10;

    num.toString(); //"10"
    num.toString(2);  //"1010"
    ```

* Math
  ```javascript
  Math.PI; //3.14159....
  Math.ceil;
  Math.floor;
  Math.round;
  Math.max;
  Math.min;
  Math.abs;
  Math.pow(n, m); //Math.pow(2, 10) //1024
  Math.sprt(n, m); //Math.sprt(16) //4      square root
  
  let userRate = 30.1234;
  userRate.toFixed(2);  //30.12
  userRate.toFixed(0);  //30
  userRate.toFixed(6);  //30.12400
  //문자열을 반환하므로 number로 변환 필수!

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

* ParseInt : Number와 다르게 문자가 혼용되어 있어도 숫자로 변환
   ```javascript
   let margin = '10px';

   ParseInt(margin);  //10
   Number(margin);    //NaN

   let redColer = 'f3';
   ParseInt(redColer);  //NaN

   ParseInt(redColer, 16);  //243

   ParseInt('11', 2);  //3
  ```

* ParseFloat : 부동소수점 반환
   ```javascript
    let padding ='18.5%';
    parseInt(padding);  //18
    parseFloat(padding);  //18.5
  ```


<br><br><br><br>

:star: 코딩애플's [자바스크립트 중급 강좌](https://www.youtube.com/watch?v=ZI6TT93wggA&list=PLZKTXPmaJk8JZ2NAC538UzhY_UNqMdZB4&index=5)를 보고 정리한 것입니다.