---
layout : single
title: "Compiling"
categories: CS50
tag: [CS50, blog, ComputerScience]
toc: true
---

> ## **수업내용**

컴퓨터가 내 코드를 이해하기 위해서는 내가 쓴 코드를 0과 1로 변환해야한다.

```c
#include <studio.h>

int main(void)
{
    printf("hello, world\n");
}
```

이러한 소스코드는 0과 1로 구성된 machine code로 변환되어야한다. 지난번 강의에서 배운 것처럼 0과 1 숫자, 글자, 색, 오디오, 비디오 등을 나타내기도하지만 출력, 삭제, 저장 등의 지시코드(construction code)를 의미하기도 한다. 이러한 숫자들이 어느 위치에 저장되어 있는지에 따라 무엇으로 해석될지를 구분한다.



![machinecode로](https://user-images.githubusercontent.com/93427305/160343211-51d53fe5-1649-4ffc-827a-7dfadd0d63ee.jpg)



computer science가 문제를 푸는 것이라 했는데 그 과정과 마찬가지로  위 처럼 source 코드를 넣으면 machine code가 결과로 나온다고 볼 수 있다. 이 과정을 우리의 손으로 변환하는 건 불가능하고 하고 싶지도 않을 것이다. 다행히도 특수한 프로그램의 알고리즘으로 이를 직접하지 않아도 된다. 이 특수한 프로그램이 바로 컴파일러(Compiler)이다. 모든 언어가 컴파일러를 사용하는 것은 아니지만 C는 컴파일러를 사용하는 언어이다. 그러므로 C를 사용한다면 컴퓨터의 어딘가에는 한 언어를 다른 언어로 변경해주는 걸 목적으로하는 컴파일러가 존재할 것이다. 
<br/><br/>


> ## **소감**

자바 또한 컴파일이 필요한 언어라서 컴파일에 대해서는 조금 안다고 생각한다. 늘 마주치던 컴파일 에러가 떠오르는 것도 이와 같은 이유일 것이다. 

