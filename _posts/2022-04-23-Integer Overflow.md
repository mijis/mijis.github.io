---
layout : single
title: "Integer Overflow"
categories: CS50
tag: [CS50, blog, ComputerScience]
toc: true
---

> ## **수업내용**

```c

#include <cs50.h>
#include <studio.h>

int main(void) 
{
    //promt user for x
    int x = get_int("x: ");

    //promt user for y
    int y = get_int("y: ");

    //perform addition
    pirntf("%i\n", x+y);
}
```


2천만 더하기 2천만을하면 -의 이상한 값이 나오는 것을 확인할 수 있다. 컴퓨터의 공간이 다 찼기 때문이다. 지금까지 배운 모든 데이터 타입을 나타내기 위해서는 한정된 비트의 크기가 있다. 컴퓨터마다 다를 수 있으나, 새 컴퓨터일 수록 더 많은 비트를 사용하고 오래된 컴퓨터일수록 적은 비트를 사용한다.

현재의 상황에서는 정수로 32bit가 사용되고 있다. 32bits로 꽤나 큰 수를 나타낼 수 있다. 저번 시간에 8개의 0과 1로 이루어진 8bits에 대해서 배운 적이 있다. 8 bit는 0과 1로 구성하여 256까지 셀 수 있다. 32는 얼마나 되는가? 2의 32승(2^32||2 to the 32)은 대략 4천만이다. 그러니 32bit가 사용되면 2천 더하기 2천은 4천이 나와야한다. 그러나 정수에는 음수가 있으므로 2천만큼 양수가 있다면 그만큼의 음수가 있어야한다. 따라서 양수와 음수의 개수의 합이 4천개가 되므로  32bit의 정수로 2천 더하기 2천을 할 수 없는 것이다. <br><br><br>



그렇다면 어떻게 4천을 나타낼 수 있을까?
```c

#include <cs50.h>
#include <studio.h>

int main(void) 
{
    //promt user for x
    long x = get_long("x: ");

    //promt user for y
    long y = get_long("y: ");

    //perform addition
    pirntf("%li\n", x+y);
}
```
첫 번째 것의 int를 long으로 변경하면 4천의 합이 나온다. 이처럼 long을 사용하면 64bit를 사용하여 음수 양수를 합한 4천 개의 수를 표현할 수 있다. 크다고 생각할 수 있지만 여전히 한정된 수이다. 모든 수의 합을 나타내기에는 부족하기 때문이다.
