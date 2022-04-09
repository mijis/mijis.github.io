---
layout : single
title: "reading errors"
categories: CS50
tag: [CS50, blog, ComputerScience]
toc: true
---


> ## **수업내용**
```c
int main(void)
{
    printf("hello, world
    ");
}

int main(void)
{
    printf("hello, world\n");
}
```
<br>

만약 "\n"을 사용하지 않고 우리가 흔히 사용하는 enter 방식으로 새 라인을 만들면 하나의 라인에서 에러가 생겼는데 10개의 에러가 나온다. 이런 에러들을 읽어야한다. <br>
→ missing terminating '""' character : c에서 string을 사용할 때에는 ""이 꼭 필요하다.
이를 방지하기 위해서는 escape sequence(확장열)란 것을 사용해야한다. 보통 \와 스페셜한 심볼, n같은 것을 같이 사용해 새로운 라인을 만들라는 의미를 가지는 걸 뜻한다. 이건 enter key 대신 \n을 쓰자란 약속된 문법이다. 암호적인 것 같지만, 알고보면 결국 우리가 알고 있는 것 다른 방식으로 사용하는 것일 뿐이다. 


<br><br><br><br>

> ## **소감**
컴퓨터의 세상을 아직 안다고 말할 수 없지만, 지금까지 배운 걸로 느끼기에 그 무엇보다 체계적이다. 논리가 있고, 순서가 있어 즐겁게 배울 수 있는 것 같다. 