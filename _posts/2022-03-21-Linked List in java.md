---
layout : single
title: "Linked List"
categories: algorithms/engineerkorea
tag:  [blog, algorithm, ComputerScience]
toc: true
---

# Linked List 구현2 in java
 저번에 구현했던 노드는 첫 노드를 삭제할 수 없다는 문제가 있었다. 헤더가 첫번째 값이면서 링크드리스트의 대표이기 때문이다. 이를 해결하기 위해선 노드 클래스를 링크드 리스트에 감싼 후 링크드 리스트에 헤더를 따로 저장하고 그 안에  노드클래스를  따로 만들어주면 된다. 


 ![linked list 안에 노드 넣기](https://user-images.githubusercontent.com/93427305/159212607-80d1aaf2-9e8e-40fd-aac7-93513007525d.jpg)
 
<br><br>
## **Java에서 구현**
 ```java
public class LinkedList {
	Node header;
	
	static class Node{
		int data;
		Node next =null;
	}
	
	LinkedList(){
		header = new Node();
	}
	
	//추가 방법
		void append(int d) {
			Node end = new Node();
			end.data=d;
			Node n = header; //포인터 위치를 헤더가 잡는다.
			
			while(n.next!=null) {//n의 다음이 없을 때까지(마지막까지)
				n=n.next; //마지막 노드를 찾는다
			}
			n.next=end; //위에서 찾은 마지막 노드의 값에 새로운 node 값을 넣어준다
		}
		
		void delete(int d) {
			Node n=header; //포인터 위치
			while(n.next!=null) {//n의 다음이 없을 때까지
				if(n.next.data==d) { //다음 노드가 d와 같으면
					n.next=n.next.next; //다음 노드에 다음다음 노드를 넣어 다음 노드가 삭제되는 결과 도출
				}else {
					n=n.next;
				}
			}
		}
		
		void retrieve() {
			Node n = header;
			while(n.next!=null) {
				System.out.print(n.data+"→");
				n=n.next;
			}
			//마지막 노드는 출력하지 않기 때문에
			System.out.println(n.data);
		}
		
	    //결과보기
		public class LinkedListNode{
			public static void main(String[] args) {
				LinkedList ll= new LinkedList();
				ll.append(1);
				ll.append(2);
				ll.append(3);
				ll.append(4);
				ll.retrieve();
				ll.delete(1);
				ll.retrieve();
			}
		}
}
 ```

포인터의 위치를 header가 이동하면 첫 번째 값도 지울 수 있게 된다. 저번 강의에서 배웠을 땐 첫 번째 값이 링크드 리스트이자 노드 그 자체여서 지울 수 없었는데 헤더를 사용하면 첫 번째 값도 지울 수 있게 된다. 정확한 비유인지는 모르겠지만, DB의 커서와 유사하다고 생각한다. 

 ### ※ 강의 듣는 곳
>https://www.youtube.com/watch?v=IrXYr7T8u_s<br>
엔지니어 대한민국 [자료구조 알고리즘] LinkedListNode의 구현 in Java를 듣고 정리한 것입니다<br>