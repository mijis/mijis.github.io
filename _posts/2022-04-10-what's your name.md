---
layout : single
title: "What's your name?"
categories: CS50
tag: [CS50, blog, ComputerScience]
toc: true
---


> ## **수업내용**

<br>

```c
int main(void)
{
    string answer = get_string("What's your name?");
    printf("hello, answer\n");
}
```
1. 위처럼 쓰면 많은 에러가 난다. 제일 첫 에러를 찾아가기 위해서 hello를 컴파일 한 바로 밑의 에러를 확인해보면 에러가 발생한 라인의 넘버와 왜 에러가 났는지에 대한 게 나온다. 
<br>
▶ use of undeclared identifier 'string' : did you mean 'stdin'? 
<br> 
위처럼 나오면서 string 대신 stdin(standar in)을 원한 것이냐고 물어본다. 이걸 보면 string 문자열을 쓰기 위해서는 다른 무엇인가가 필요하다는 걸 깨달을 수 있다.

<br>

 ```c
#include <cs50.h>
#include <studio.h>

int main(void)
{
    string answer = get_string("What's your name?");
    printf("hello, answer\n");
}
```
2. 위와 같이 #include <cs50.h> 라이브러리를 추가해주면 에러가 나지 않는다. 이것에 대해 알아보기에 좀 앞서, standar I/O가 무엇인지 알아야한다. 특정한 function, 즉 printf 같은 action이나 verb을 사용하고 extension을 load해야한다. 이걸 library라고 한다. standard I/O, STD I/O가 있다. I/O는 input과 output을 뜻하는데, scratch에서 봤던 텍스트를 음성으로 변환하는 일과 같이 extension이라고 볼 수 있다. c에서의 extension이 바로 library이다. 키보드와 관련된 기능을 사용하고 싶다면 studio.h를 꼭 써줘야 printf의 기능을 사용할 수 있다. library에 대해서는 나중에 더 알아보겠지만, standar I/O는 printf에 대한 접근을 가능하게 해주는 라이브러리라는 것과 input and output-과 관련된 것이라는 건 꼭 알고 넘어가야한다. CS50.h는 c에서는 할 수 없는 기능들을 가능하게 해주는 두 번째 라이브러리이다.  두 번째 코드에서  make hello를 하고 ./hello를 실행시키면, "what's your name?"이 콘솔창에 뜬다. 그리고 내가 옆에 무엇인가를 입력하더라도 "hello, answer"이 콘솔창에 뜰 것이다.  그렇다면 변수 answer를 printf에 넣어주려면 어떻게 해야하는가?


<br><br><br><br>

> ## **소감**
아주 기초를 배우고 있다는 걸 알지만, 코드 한 줄 틀렸는데 그렇게 수많은 에러가 나왔다는 걸 보니 감회가 새롭다. 에러 읽기를 주저하지 말아야겠다.