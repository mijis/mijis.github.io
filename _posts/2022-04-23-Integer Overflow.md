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


2천만 더하기 2천만을하면 -의 이상한 값이 나오는 것을 확인할 수 있다.



<br><br><br><br>

> ## **소감**