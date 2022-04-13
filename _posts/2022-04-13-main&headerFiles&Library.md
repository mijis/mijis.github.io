---
layout : single
title: "Main & Header File & Library"
categories: CS50
tag: [CS50, blog, ComputerScience]
toc: true
---

> ## **수업내용**

<br>

```c
int main(void)
{

}
```
1. main <br>
scratch에서 배웠던 when flag clicked(깃발이 클릭되면)과 가장 유사한 건 write out(쓰다)란 의미일 것이다. c 프로그래머로서 제일 처음 하는 일은 빈 파일을 하나 생성하고, 위와 같은 형식을 만든 후 {}중괄호 안에 코드를 적어 나갈 것이다. c는 텍스트를 기반으로 한 것으로 {가 열렸다면 닫아주는 }가 필요하고 그 안에 적힌 것들은 모두 main에 포함된다. 
<br>
<br>

```c
# include <studio.h>

int main(void)
{

}
```
2. 컴파일러에게 알려주기<br>
scratch엔 문법이 없었다. 그래픽으로 표현되어서 그냥 드래그만 하면 됐지만, c는 문법이 필요하다. 출력하고 싶다고 해서 그냥 printf한다고 해서 절대 원하는 대로 표현되지 않을 것이다. #include <studio.h>가 있어야 컴파일러에게 라이브러리를 로드하라고 명령을 해야 컴퓨터는 printf가 무엇을 뜻하는지 알아들을 것이다. 또 get_string이나 다른 함수를 사용하고 싶다면 그에 맞는 library를 다운받아야 사용할 수 있다. 

3. 파일 이름
studio.h, cs50.h 같은 파일은 header file이라 불린다. 나중에 더 자세히 알아보겠지만, 이 파일에는 이 파일을 가져옴으로서 사용할 수 있는 모든 종류의 함수가 메뉴처럼 나열되어 있다. 

4. 다음주에 배우겠지만, library와 header file은 완전히 동일한 것은 아니다. 간략히 알아보면 library는 standard I/O, CS50이고 그에 상응하는 header file이 각각 studio.h, cs50.h인 것이다. 

5. c에서는 string이 default type으로 존재하지 않는다. 

<br><br><br><br>

> ## **소감**
오늘 c언어를 치면서 무의식적으로 괄호를 void 옆에 붙였다. 별 것은 아니지만 습관이란게 생겼다는게 조금 뿌듯했다. 나도 library와 header file이 똑같다고 생각했는데 수강생 중에 한 명이 질문해주어서 알게되었다. 기능 위주로 배우다보니 이런 점들은 놓치고 있을 때가 많은데 점점 알게 되는 게 좋다. 