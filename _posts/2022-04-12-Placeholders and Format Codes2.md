---
layout : single
title: "Placeholder and Format Codes_2"
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
    printf("hello, %s\n", answer);
}
```

1. printf 안에서 변수를 선언할 수 있는가? 불가능하다.

2. string은 무엇인가? string은 변수의 타입으로 정확히는 데이터 타입이다.

3. get_string("What's your name?") 앞에 string을 사용할 수 있는가? 데이터 타입은 변수 앞에서만 사용할 수 있다.


```c
int main(void)
{
    printf("hello, get_string("What's your name?"));
}
```

4. 위처럼 변수를 사용하지 않고 바로 대입할 수 있는가? 가능하다. 하지만 이게 더 나은 코드인지에 대해서는 생각해봐야한다. 오랜 시간 토론할 수 있는 주제이지만, 가장 큰 차이점은 변수를 사용하면 한 번 정의하여 여러 번 사용할 수 있고, 위처럼 쓰면 같은 코드를 계속 길게 써야하는 문제가 있다.

5. 지금까지 input output으로 배웠었지만, 더 면밀하게 보면 input은 arguments, parameter이고 output은 return value이다. return value는 function에서 나온 값을 또 한 번 사용할 수 있게 해준다. output의 function이 다른 function의 input으로 사용될 수 있다는 걸 scratch에서 배웠었다. c의 방식은 조금 다르지만 개념은 똑같다.

    ![arguments, reurn value](https://user-images.githubusercontent.com/93427305/162971793-5fb9a1e7-1933-4646-bfad-afb665e51b08.jpg)

<br><br><br><br>

> ## **소감**
알고 있는 개념들이지만, 세세하게 짚고 넘어가서 컴퓨터 언어를 좀 더 깊게 이해할 수 있을 것 같아서 좋다.
