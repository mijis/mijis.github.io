---
layout : single
title: "calculator.c"
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
    int x = get_int("x: ");
    int y = get_int("y: ");
    pirntf("%i\n", x+y);
}
```

x와 y 변수에는 각각 사용자가 입력한 x,  y의 값이 들어간다. x와 y의 합을 알고 싶다면 현실에서는 x+y라하면 되겠지만, printf의 값은 ""안에 들어간 string이어야한다. 전에 배운 것 중에 integer로 변환할 수 있는 기호가 있었다. %i를 사용하여 ""안에 integer가 들어갈 것임을 알려주고 그 값은 x와 y의 합이라고 , 뒤에 써주면 된다.


<br><br>


```c

#include <cs50.h>
#include <studio.h>

int main(void) 
{
    int x = get_int("x: ");
    int y = get_int("y: ");
    int z = x + y ;
    pirntf("%i\n", z);
}
```

이렇게 해도 첫 번째와 같은 결과가 나온다. 그렇다면 어디가 더 좋은 디자인일까?<br>
그건 의도에 따라 다르다. 두 번째 코드는 x+y의 값을 다시 사용하려한다면 좋은 값이다. 그와 반대로 첫 번째 코드는 직관적이므로 x+y가 다시 사용될 일이 없다면 더 알아보기가 쉽다. 장단점이 있는 것이다. 또한 x와 y처럼 널리 쓰이는 이름은 굳이 first_number이런 식으로 쓸 필요 없이 x,y로 쓰는 것이 훨씬 코드를 단축시켜줄 수 있다.



<br><br><br><br>

> ## **소감**
기초이지만 다시 들으면서 정리가 되어 만족스럽다. 이름을 주는 게 참 어렵다고 느껴질 때가 있었는데 너무 부담을 가지지 않고 주도록해야겠다.