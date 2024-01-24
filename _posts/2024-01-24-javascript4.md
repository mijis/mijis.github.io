---
title: javascript_4
date: 2024-01-24 21:20:27 +0900
categories: [javascript]
tags: [js]
---

### 🌟 Symbol

* property key = 문자형
    ```javascript
    const obj = {
      1: '1입니다',
      false: '거짓'
    }

    Object.keys(obj); //["1", "false"] : 문자형으로 반환

    //접근 시에도 문자로 접근
    obj["1"]  //'1입니다'
    obj["false"]  //'거짓'
    ```

* Symbol = 유일한 식별자! / 유일성 보장
  ```javascript
  const a = Symbol(); //new 를 붙이지 않음!!!!
  const b = Symbol(); //new 를 붙이지 않음!!!!

  console.log(a);
  console.log(b);

  a===b; // false
  a==b;  // false

  const id = Symbol('id');
  const id2 = Symbol('id');

  id //Symbol(id);
  id //Symbol(id);

  id === id2 // false
  id == id2  // false


  const user = {
    name: 'MIKE',
    age: '20',
    [id]: 'myid'
  }

  user //{name: 'MIKE',  age: '20', Symbol(id):"myid"}
  user[id] // "myid"

  //Symbol 생략
  Object.keys(user);  //["name", "age"]
  Object.values(user);  //["MIKE", 20]
  Object.entries(user);  //[Array(2), Array(2)]
  //for in 도 Symbol 생략
  ```
  + 특정 객체에 원본을 건드리지 않고 속성 추가 가능! <br><br>


* Symbol.for() : 전역 심볼
  + 하나의 심볼만 보장
  + 없으면 만들고, 있으면 가져옴
  + Symbol 함수는 매번 다른 Symbol 값을 생성
  + Symbol.for 메소드는 하나를 생성한 뒤 키를 통해 같은 Symbol **공유**
  ```javascript
    const id1 = Symbol.for('id');
    const id2 = Symbol.for('id');

    id1 === id2;  //true

    //이름 사용
    Symbol.keyFor(id1)  //"id"
    id.description; //'id'  //이름을 알 수 있음
  ```

* 숨겨진 Symbol key 보는 법 
   ```javascript
   const id1 = Symbol.for('id');

   const user = {
    name:"Mike",
    age: 30
    [id]: 'my'
   }

   Object,getOwnPropertySymbols(user); //[Symbol(id)]
   Reflect.ownKeys(user); //모든 키를 볼 수 있음
  ```
 



<br><br><br><br>

:star: 코딩애플's [자바스크립트 중급 강좌](https://www.youtube.com/watch?v=E9uCNn6BaGQ&list=PLZKTXPmaJk8JZ2NAC538UzhY_UNqMdZB4&index=4)를 보고 정리한 것입니다.