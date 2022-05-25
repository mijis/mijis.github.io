---
layout : single
title: "conditions"
categories: CS50
tag: [CS50, blog, ComputerScience]
toc: true
---

> ## **수업내용**
```c
   if (x < y)
    {
        printf("x is less than y\n");
    }
```
위의 if는 printf의 코드를 감싸고 있다고 볼 수 있다. ()는 {}안의 내용을 실행할지말지 물어보고 결정을 내려주는 조건이다. 보통 단어와 () 괄호를 보면 함수일 수 있다. 그러나 예외가 있는데 if에서는 ()는 함수가 아니고 ()안의 값을 boolean으로 물어보는 것이다. 
<br><br>

```c
   if (x < y)
    {
        printf("x is less than y\n");
    }else
    {
        printf("x is not less than y\n");
    }
```
두 가지 조건이 있다면 위처럼 else를 써서 나타낼 수 있을 것이다. C에서 보통 한 줄의 코드만 있다면, {} 중괄호를 잘 쓰지 않지만, 연습을 위해 이렇게 나타냈다. 
<br><br>

```c
   if (x < y)
    {
        printf("x is less than y\n");
    }
    else if
    {
        printf("x is greater than y\n");
    }
    else if
    {
        printf("x is equal to y\n");
    }
```

3가지의 조건을 나타내기 위해서 else if를 사용하여 여러 조건을 쓸 수 있다. 위의 코드는 맞기는 하지만 최선의 코드라고 볼 수 없다. 정수를 비교하는 데 남는 조건은 적거나 많거나 같다로 결과가 3가지밖에 없으므로 마지막 코드는 굳이 else if를 사용하지 않고 else만 사용하여도 충분하기 때문이다. 그런데 위와 같이 코드를 치면 모두 3번의 질문을 하게 된다. 만약 x와 y의 값이 동일하다면, 첫 번째 조건을 물어 false, 두 번째 조건을 물어서 false, 세 번째에 와서야 true의 결론이 난다.
<br><br>


```c
   if (x < y)
    {
        printf("x is less than y\n");
    }
    else if
    {
        printf("x is greater than y\n");
    }
    else
    {
        printf("x is equal to y\n");
    }
```
만약 이렇게 else로 바꾼다면, 두 번의 질문으로 동일한 결과를 나타내게 된다.
<br><br><br><br>

> ## **소감**
사소하다면 사소할 수 있는 일이지만, 좋은 코드를 짜기 위해서는 중요하다. 글을 쓸 때에도 단어 하나로 전혀 다른 어투가 되듯, 코드도 똑같은 것 같다. 
