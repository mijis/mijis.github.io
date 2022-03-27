---
layout : single
title: "Linked List"
categories: engineerkorea
tag:  [blog, algorithm, ComputerScience]
toc: true
---

컴퓨터에 자료를 저장하는 구조의 한 종류로 다음 데이터의 주소를 가지고 있다.

<!-- <img scr="https://user-images.githubusercontent.com/93427305/158141536-281c6fba-dc59-4777-b033-6ed0136cde94.png" > -->

<figcaption>Liked List</figcaption>

![linked_list](https://user-images.githubusercontent.com/93427305/158141536-281c6fba-dc59-4777-b033-6ed0136cde94.png )

<figcaption>array</figcaption>

![array](https://user-images.githubusercontent.com/93427305/158141544-9b6aec28-224f-4863-b0d6-dff6d184a1f2.jpg)

<p>
배열과 비교를 하자면 배열은 방들이 물리적으로 한 공간에 모여 있어, 한 번 정하면 방을 줄이거나 늘릴 수가 없다. 그에 반해 Linked List는 중간에 데이터를 삽입하고 싶다면 앞의 노드가 가지고 있던 주소를 삽입되는 것이 가져가고 앞의 노드에게는 다음이 삽입되는 주소라는 걸 알려주면 된다. 반대로 링크를 빼고 싶다면 정확히 반대로 하면 된다. 그러나 삭제된 노드는 링크드 리스트에서만 삭제되었을 뿐, 메모리에는 여전히 존재한다. 자바에서는 이렇게 안 쓰이는 변수를 garbage collector로 자동 처리되지만 c나 C+에서는 반드시 따로 명시해야한다.
</p>
<p>
링크드 리스트는 주소를 찾아다녀야하기 때문에 배열보다 속도가 느릴 수 있다. 하지만 배열에 추가작업을 한다면 추가할 때마다 배열을 통째로 다시 선언해서 복사하는 더 복잡한 방식을 써야하므로 길이가 정해지지 않은 데이터를 쓸 때에는 Linked List가 적합하다.
</p>

---

### ※ 강의 듣는 곳
>https://www.youtube.com/watch?v=DzGnME1jIwY <br>
엔지니어 대한민국 [자료구조 알고리즘] Linked List를 듣고 정리한 것입니다.<br>

