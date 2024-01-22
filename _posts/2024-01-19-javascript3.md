---
title: javascript_3
date: 2024-01-22 22:30:27 +0900
categories: [javascript]
tags: [js]
---

### 🌟 Object method

1. computed property, 계산된 프로퍼티
     * key의 값이 유동적일 때 유용
    ```javascript
    let a = 'age';

    const user = {
      name : 'sheldon',
      [a] : 30          // ==> age : 30 변수 a에 할당된 값이 들어감
    }

    //식 자제 사용 가능
    const user1 = {
      ['안녕'+'하세요'] : 'Hello',
      [1+3] : 4          
    }

    ```
<br><br>

2. 객체 함수
   * Object.assign()
      ```javascript
      const user = {
        name : 'sheldon',
        [a] : 30          // ==> age : 30 변수 a에 할당된 값이 들어감
      }

      //user변수에는 객체가 저장된 메모리 주소인 참조값이 저장되므로 복제가 아님
      // user와 cloneUser는 같은 객체를 가리키는 중
      const cloneUser = user;

      const newUser = Object.assign({}, user); //빈객체 초기값에 두 번째 변수들이 병합 
      new User != user; // true

      Object.assign({gender:'male'}, user); //총 세 개의 property를 가지게 됨
      Object.assign({name:'maple'}, user);  //뒤의 값으로 덮어쓰임

      const user1 = {
        name : 'Mike'
      }
      const info1 = {
        age : 30
      }
      const info2 = {
        gender : 'Male'
      }

      Object.assign(user1, info1, info2); //user1에 뒤의 object 병합 가능

      ```
       <br>

   * Object.keys()
   * Object.values()
      ```javascript
      const user = {
        name : 'sheldon',
        age : 30,
        gender : 'male'
      }

      Object.keys(user); //["name", "age", "gender"]
      Object.values(user); //["sheldon", 30, "male"]
      ```
       <br>

   * Object.entries()
      ```javascript
      const user = {
        name : 'sheldon',
        age : 30,
        gender : 'male'
      }

      Object.entries(user); //  [   
                            //    ["name", "sheldon"],
                            //    ["age", 30],
                            //    ["gender", "male"]
                            //  ]
      ```
      <br>

   * Object.fromEntries()
      ```javascript
      const user = 
        [   
            ["name", "sheldon"],
            ["age", 30],
            ["gender", "male"]
        ]


      Object.fromEntries(user);
      //  {
      //    name : 'sheldon',
      //    age : 30,
      //    gender : 'male'
      //  }
      ```
 
  
<br><br><br><br>

:star: 코딩애플's [자바스크립트 중급 강좌](https://www.youtube.com/watch?v=6NZpyA64ZUU&list=PLZKTXPmaJk8JZ2NAC538UzhY_UNqMdZB4&index=3)를 보고 정리한 것입니다.