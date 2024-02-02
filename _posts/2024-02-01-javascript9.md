---
title: javascript_9
date: 2024-02-01 23:58:00 +0900
categories: [javascript]
tags: [js]
---

### 🌟 나머지 매개변수

* 인수 전달 : 개수 제한이 없고, 에러가 발생하지 않음
  ```javascript
  function showName(name){
    console.log(name);
  }
  showName('Mike'); 
  showName('Mike', 'Tom');  //에러 발생X
  showName();  //undefiend 반환

  //함수의 인자를 얻는 방법 : arguments와 나머지 매개변수 
  ```

* arguments  
  * 함수로 넘어 온 모든 인수에 접근
  * 함수 내에서 이용 가능한 지역변수
  * length / index
  * Array 형태의 객체
  * 배열의 내장 메서드 없음 (forEach, map)
  ```javascript
  function showName(name){
    console.log(argument.length);
    console.log(argument[0]);
    console.log(argument[1]);
  }
  showName('Mike', 'Tom');  
  // 2
  // Mike
  // Tom
  ```

* 나머지 매개변수 Rest parameters : 배열로 메서드 사용 가능
  ```javascript
  function showName(...names){
    console.log(names);
  }
  showName(); //[]
  showName('Mike'); //[Mike]
  showName('Mike', 'Tom'); //[Mike, Tom]

  function add(...numbers){
    let result = 0;
    numbers.forEach((num) => (result += num));
    console.log(result);
  }

  add(1, 2, 3); //6
  add(1, 2, 3, 4, 5, 6, 7, 8, 9, 10); //5 
  ```
* user 객체를 만들어주는 생성자 함수
  * 매개변수 마지막에 넣어줘야함
  ```javascript
  function User(name, age, ...skills){
    this.name = name;
    this.age = age;
    this.skills = skills;
  }

  const user1 = new User("Mike", 30, "html", "css");
  const user1 = new User("Tom", 20, "JS", "React");
  const user1 = new User("Jane", 25, "English");
  ```



<br><br><br><br>

:star: 코딩애플's [자바스크립트 중급 강좌](https://www.youtube.com/watch?v=lekNM8ldxno&list=PLZKTXPmaJk8JZ2NAC538UzhY_UNqMdZB4&index=10)를 보고 정리한 것입니다.