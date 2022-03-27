---
layout : single
title: "Linked List 구현 in java"
categories: engineerkorea
tag:  [blog, algorithm, ComputerScience]
toc: true
---

## **노드란?**
<div>
강의를 듣기 전 노드(node)에 대한 개념이 정확히 모르겠어서 않아 찾아봤다. 노드는 객체로 데이터와 다른 노드의 주소(reference)를 가질 수 있다.

![node란](https://user-images.githubusercontent.com/93427305/158795634-772c1562-5186-4363-9caf-7a3dcc83ed6f.jpg) <br/>

→ 위의 그림 처럼 하나의 노드에는 데이터와 연결될 노드 주소를 가지고 있다. <br/><br/>


![노드의 연결](https://user-images.githubusercontent.com/93427305/158795640-87378414-e100-4eee-9f1f-567351be7401.jpg)

→  앞서 배운 단방향 linked list를 노드로 나타내면 이렇게 그려질수 있다.
</div>


<br/><br/><br/><br/>


## **Java에서 구현**

```java
public class Node {

	int data;
	Node next=null;
	
	Node(int d){
		this.data=d;
	}
	
	//추가 방법
	void append(int d) {
		Node end = new Node(d);
		Node n = this; //포인터 위치를 잡고
		
		while(n.next!=null) {//n의 다음이 없을 때까지(마지막까지)
			n=n.next; //마지막 노드를 찾는다
		}
		n.next=end; //위에서 찾은 마지막 노드의 값에 새로운 node 값을 넣어준다
	}
	
	void delete(int d) {
		Node n=this; //포인터 위치
		while(n.next!=null) {//n의 다음이 없을 때까지
			if(n.next.data==d) { //다음 노드가 d와 같으면
				n.next=n.next.next; //다음 노드에 다음다음 노드를 넣어 다음 노드가 삭제되는 결과 도출
			}else {
				n=n.next;
			}
		}
	}
	
	void retrieve() {
		Node n = this;
		while(n.next!=null) {
			System.out.print(n.data+"→");
			n=n.next;
		}
		//마지막 노드는 출력하지 않기 때문에
		System.out.print(n.data);
	}
	
    //결과보기
	public class SinglyLinkedList{
		public static void main(String[] args) {
			Node head = new Node(1);
			head.append(2);
			head.append(3);
			head.append(4);
			head.retrieve();
			System.out.println();
			head.delete(2);
			head.retrieve();
	
		}
	}
}
```
※ n의 다음 노드부터 비교하면 첫번째 노드는 비교하지 않고 넘어간다. 헤더는 값을 비교하기 이전에 링크드 리스트를 대표하는 첫번째 노드이기 때문에 첫번째 헤더를 지우면 다른 오브젝트가 삭제된 헤더를 갖고 있는 경우 문제가 생기게 되므로 첫번째 노드는 지금은 지우지 않는다.


### ※ 강의 듣는 곳
>https://www.youtube.com/watch?v=C1SDkdPvQPA<br>
엔지니어 대한민국 [자료구조 알고리즘] 단방향 Linked List 구현 in Java를 듣고 정리한 것입니다<br>