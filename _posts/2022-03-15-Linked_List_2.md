---
layout : single
title: "Linked List"
categories: engineerkorea
tag:  [blog, algorithm, ComputerScience]
toc: true
---
# 단방향, 양방향 Linked List

1. 단방향 Linked List
![단방향 linked_list](https://user-images.githubusercontent.com/93427305/158332202-312d9074-1f9c-42be-8154-5ca5568fb8a2.jpg)
위의 링크드 리스트를 보면 한쪽 방향으로만 화살표가 되어 있어, 자료는 한방향으로만 갈 수 있다. 가운데 노드는 앞의 주소는 모르고 오직 뒤의 주소만 알 수 있는 뜻이다. 따라서 검색을 할 때에는 가장 앞에서 한 개씩 노드를 이동하며 검색해야한다. 이렇게 한 방향으로만 이동할 수 있는 Linked List를 단방향 Linked List라고 한다.
<br>
<br>
2. 양방향 Linked List
![양방향 linked_list](https://user-images.githubusercontent.com/93427305/158332197-2edcd52a-078d-4b12-9da8-2a24793967c9.jpg)
![양방향 linked_list 노드 삽입](https://user-images.githubusercontent.com/93427305/158401482-4961d5b2-f6a9-40ff-88ba-080d330d4992.jpg)
위의 첫 그림처럼 양방향 Linked List는 다음 주소를 가지고 있을뿐 아니라 앞의 노드 주소도 가지고 있다. 이로 인해 앞 뒤로 자유롭게 이동할 수 있다. 여기에 새로운 노드를 삽입하기 위해서는 위의 두 번째 그림처럼 앞 뒤의 주소를 가져오고 자신의 주소를 앞뒤로 보내주면 된다. 단방향 삽입과 똑같지만 앞의 노드에 자신의 주소르 보내고, 뒤의 주소 또한 가져온다는 것만 다르다. 양방향 Linked List는 양쪽 끝에 주소를 저장하고 있어 맨 끝에 노드를 삽입할 때 단방향 Linked List와 달리 찾는데 걸리는 시간을 줄일 수 있다. 
<br>
<br>
3. 결론
양쪽으로 이동할 필요가 없는 데이터는 굳이 양방향 링크드 리스트를 사용할 필요가 없다. 이처럼
효율성을 생각해서 어느 알고리즘이 필요한지 파악하고 상황에 맞춰서 쓰면된다.
<br>
<br>
### ※ 강의 듣는 곳
>https://www.youtube.com/watch?v=DzGnME1jIwY <br>
엔지니어 대한민국 [자료구조 알고리즘] Linked List를 듣고 정리한 것입니다.<br>