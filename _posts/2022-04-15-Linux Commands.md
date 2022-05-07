---
layout : single
title: "Linux Commands"
categories: CS50
tag: [CS50, blog, ComputerScience]
toc: true
---

> ## **수업내용**

<br>

리눅스의 세계에서는 명령어의 대략적인 리스트들이 있는데(non-exhaustive list of commands) 몇 주 안으로 문제를 풀면서 익숙해질 것이다.  <br>

    1. ls : list
    2. rm : others
    3. cp : copy
    4. mkdir  : make directory
    5. mv  : move or remove
    6. rmdir : remove directory
    7. cd : change directory
    8. ctrl + L / clear : window clear 
    9. cd .. : 뒤로가기

 GUI(Graphical User Interface)에서는 컴퓨터를 사용해왔던 그대로 폴더를 생성하고 안에 파일을 넣으면 된다. command line에서도 이와 똑같은 작업을 할 수 있는데, ls를 치면 [hello* hello.c pset1/] 이렇게 나온다. hello*하고 초록색 글자로 된 것은 실행할 수 있는 파일이라는 뜻이고 .c파일은 나의 소스 코드란 의미이다. 또 파란색 글자로 pset1/ 폴더명과 슬래시가 함께 적히는 것은 폴더라는 걸 알려준다. <br>

 커맨드 창에 [mkdir 파일명]을 적고 엔터를 누르면 폴더가 생성되는 것을 확인할 수 있다. 만약 cd pset1(파일명)이라고 친다면 [$ ]이라고 나오던 프롬프트 창에 [pset1/ $ ]이 나오는 것을 확인할 수 있다. 현재 나의 위치가 어디인지 알려주는 것이라고 보면 된다. 현재 상태에서 mkdir mario를 친다면, pset1 폴더 아래 mario라는 폴더가 형성될 것이다. mario 폴더 안에서 mario.c 파일을 만들고 싶다면 code mario.c를 치면 mario 폴더 아래 mario.c 파일이 만들어질 것이다. <br>

 만약 뒤로 가고 싶다면 어떻게해야할까? ..은 부모 폴더로 가라는 의미이다. pset1/mario/ $ 상태에서 cd ..을 친다면 mario 폴더의 부모 폴더, 상위폴더인 pset1/ $로 이동하는 것을 확인할 수 있다. 만약 pset보다 더 위의 폴더로 가고 한 번에 가고 싶다면 cd ../..을 하면 한 번에 pset 상위폴더로 이동한다. 하지만 그냥 cd만 쳐도 default folder로 이동할 수 있다.

 ./hello를 사용하는 이유는 현재 내가 위치한 곳에서 hello 파일을 실행시키라는 의미를 컴퓨터에게 정확하게 전달하기 위함이다. 

 <br><br><br><br>

> ## **소감**
리눅스 명령어를 잘 모를 때에 command line을 통해 깃을 사용하는게 너무 어렵게만 느껴졌다. 지금도 편리하게 사용한다고는 할 수 없지만, 심리적 거리감은 줄어든 것 같다. 