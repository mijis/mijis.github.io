---
title: javascript_1
date: 2024-01-18 22:20:27 +0900
categories: [javascript]
tags: [js]
---

### 🌟 생성자 함수

* Object Literal(변하지 않는 값)
    ```javascript
    let user = {
      name : 'Mike',
      age : 30,
    }
    ```

* 생성자 함수
  ```javascript
  function User(name, age){ //첫글자 대문자로 하는 함수  
    this.name = name;
    this.age = age;
  }

  let user1 = new User('Mike', 20);
  let user1 = new User('Jane', 30);
  let user1 = new User('Tom', 32);
  ```

* 함수 호출 시 생성자 함수의 동작 과정
  ```javascript
    function User(name, age){ //첫글자 대문자로 하는 함수 
      //1. this = {}; 
      this.name = name;
      this.age = age;
      //return 
    }

    new 함수명();
  ```

* 생성자 함수에 method 
   ```javascript
    function User(name, age){ //첫글자 대문자로 하는 함수 
      this.name = name;
      this.age = age;
      this.sayNmae = function(){
        console.log(this.name);
      }
    }

     let user5 = new User('apple', 40);
     user5.sayNmae();
  ```
  - user5.sayNmae(); :arrow_right: sayName 함수 내부 this는 **user5**이다.

* 생성자 함수 new를 붙이지 않고 실행하면 함수를 실행한 것과 동일하게 작동하므로 return 값이 없는 것과 마찬가지이다. 



<br><br><br><br>

:star: 코딩애플's [자바스크립트 중급 강좌](https://www.youtube.com/watch?v=8hrSkOihmBI&t=2s)를 보고 정리한 것입니다.