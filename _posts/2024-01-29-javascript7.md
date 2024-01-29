---
title: javascript_7
date: 2024-01-29 20:11:00 +0900
categories: [javascript]
tags: [js]
---

### 🌟 Array

* arr.splice(n, m) : 특정 요소 지움 - n부터 m개
    ```javascript
    let arr = [1,2,3,4,5];
    arr.splice(1,2);

    console.log(arr); //1,4,5
    ```

* arr.splice(n, m, x) : 특정 요소 지우고 추가
  ```javascript
  let arr = [1,2,3,4,5];
  arr.splice(1, 3, 100, 200);

  console.log(arr); //[1, 100, 200, 5]
  ```

* arr.splice() : 삭제된 요소 반환
  ```javascript
  let arr = [1,2,3,4,5];
  let result = arr.splice(1, 2);

  console.log(result);  //[2, 3]
  ```

* arr.slice() 
  ```javascript
  let arr = [1,2,3,4,5];
  let arr2 = arr.splice();

  console.log(result);  //[1,2,3,4,5]
  ```

* arr.concat(arr2, arr3...) 
  ```javascript 
  let arr = [1,2];
  aarr.concat([3,4], 5,6);  //[1,2,3,4,5,6]
  ```

* arr.forEach(fn) 
  ```javascript 
  let users = ['Mike', 'Tom' , 'Jane'];
  users.forEach((itme, idx, arr) => {
    // 
  });

* arr.indexOf/ arr.lastIndexOf
  ```javascript 
  let arr = [1, 2, 3, 4, 5, 1, 2, 3];
  arr.indexOf(3, 3);  //7
  ```

* arr.find(fn)  / arr.findIndex(fn)
  * 첫 번째 true만 반환, 존재하지 않을 때  undefined
  * 배열 안 객체 사용 시 find 가능
  
* arr.filter() : 모든 객체에 대해서 조건에 일치하는 것을 찾을 때
  
* arr.reverse() : 역순 정렬
  
* arr.map() : 특정 기능을 수행하고 새로운 array 반환
 
* arr.join() : 파라미터에 넣어주는 값으로 합쳐짐(기본 ,)
  
* arr.isArray() : typeof 사용시 모두 Object 반환하므로

* arr.sort() - ladash 참고!!
  * 배열 자체 재정렬 
  * 인수로 정렬 로직을 담은 함수 받음 
  ```javascript 
  let arr = [1, 5, 4, 2, 3]; 
  arr.sort();
  console.log(arr); // [1 2, 3, 4, 5]
  
  let arr2 = [27, 8, 5, 13]; 
  arr2.sort(fn(a,b){
    return a-b;
  });
  console.log(arr2); // [1 2, 3, 4, 5]
  
  ```

* arr.reduce()
  * 인수로 함수를 받음 
  * (누적 계산 값, 현재값) => {return 계산값};
  * 초기값으로 배열 받을 수 있음
  ```javascript 
  let arr = [1, 2, 3, 4, 5]; 
  
  let result = 0;
  arr.forEach(num => {
    result += num;
  });
  ```

  ```javascript 
  let userList = [
    {name : "Mike", age: 30}, 
    {name : "Tom", age: 23}, 
    {name : "Jane", age: 40}, 
    {name : "Harry", age: 3}, 
    {name : "Steve", age: 12}
  ];

  let result = userList.reduce((prev, cur) => {
    if(cur.age > 19){
      prev.push(cur.name);
    }
    return prev
  }, []);
  
  let result = 0;
  arr.forEach(num => {
    result += num;
  });
  ```
   
  

<br><br><br><br>

:star: 코딩애플's [자바스크립트 중급 강좌](https://www.youtube.com/watch?v=pJzO6O-aWew&list=PLZKTXPmaJk8JZ2NAC538UzhY_UNqMdZB4&index=7&t=17s)를 보고 정리한 것입니다.