---
layout : single
title: "Linked List"
categories: engineerkorea
tag:  [blog, algorithm, ComputerScience, engineerkorea]
toc: true
---

# Linked List 중복값 삭제
문제 : 정렬되어있지 않은 LinkedList의 중복값 제거. (단, 버퍼를 따로 사용하지 않는다.)
<br/><br/>

![linkedlist 중복값 삭제_buffer](https://user-images.githubusercontent.com/93427305/160135890-edc9e08f-ab88-4e09-879a-2fb399f897ab.jpg)
space(버퍼공간): O(N)만큼 사용. N은 리스트의 길이. 가진 리스트의 아이템에 비례한다는 뜻<br/>
Time(시간) : O(N). 루프를 한 번만 돌면되기 때문에.
<hr/><br/><br/>

그러나 문제에서 버퍼공간을 사용하지말라했기 때문에 다른 방식이 필요하다. 
![linkedlist 중복값 삭제_runner](https://user-images.githubusercontent.com/93427305/160135901-2b499616-31b5-493f-9112-e78184f35792.jpg)

위처럼 node와 runner 두 개의 포인터를 사용하면 따로 공간을 쓰지 않고, 중복값을 삭제할 수 있다.
<hr/><br/><br/>


```java
```








++ 추가 지식

**버퍼(buffer)** : 데이터를 한 곳에서 다른 한 곳으로 전송하는 동안 일시적으로 그 데이터를 보관하는 메모리의 영역<br/>
**버퍼링(buffering) 또는 큐(Queue)** : 버퍼를 활용하는 방식 또는 버퍼를 채우는 동작<br/>
(https://ko.wikipedia.org/wiki/%EB%B2%84%ED%8D%BC_(%EC%BB%B4%ED%93%A8%ED%84%B0_%EA%B3%BC%ED%95%99))
