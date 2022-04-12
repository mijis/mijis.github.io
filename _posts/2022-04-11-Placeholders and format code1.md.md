---
layout : single
title: "Placeholder and Format Codes_1"
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
1. 변수를 printf에 넣기 위해서는 어떻게 해야하는가? placeholder, format code를 넣어줘야한다. printf 안에 answer 대신 %s를 넣어줘야한다. %s는 컴퓨터에게 이 자리는 string의 자리임을 알리는 표현이다. ""자리 밖에 ,를 쓴 후 컴퓨터가 %s의 자리에 넣어주기를 원하는 변수의 이름을 쓰면 변수 answer가 "hello, 변수" 이렇게 들어가는 것을 확인할 수 있다. 따라서  %s는 format code로 placeholde의 역할을 하는 것이다.

2. 위의 printf는 몇 개의 input을 가지고 있는 것인가? 2개이다. 두 번째 ,를 기점으로 앞의 "hello, %s\n" 하나, 뒤의 answer 두 개해서 총 2가지의 input을 가지고 있다. 확인을 위해서 왜 첫 번째 ,는 하나의 input으로 치지않는가? 첫 번째 ,는 그저 문자열 안의 영어 문법이었을 뿐이므로 컴퓨터 언어와 관련이 없다. 현실에서의 언어와 같은 걸 쓰지만 문법은 다르기 때문에 프로그래밍에서 다소 헷갈릴 수 있다.

3. 위에서처럼 글자들의 색이 다른 것을 확인할 수 있다. 이는 vs code 같은 에디터들이 하이라이터를 쳐주기 때문이다. 텍스트 에디터가 이게 무슨 언어인지 알기만한다면, 이렇게 다양한 아이디어들을 다른 색으로 하이라이트해서 보여준다. 이 하이라이트는 실수가 가시화되고 하나의 괄호를 선택하면 그 괄호에 상응하는 괄호를 하이라이트해서 보여주기 때문에 긴 코드에서 여기가 어디인지 빠르게 알아낼 수 있다. vs 코드에서는 점과 선을 통해서 tab이 되는 게 정말로 잘 보인다. 




<br><br><br><br>

> ## **소감**
강의에서는 vs code가 쓰였지만, 내가 쓰고 있는 이클립스나 markdown에서는 조금 다르다. 이클립스에서는 하이라이트는 잘 적용되지만, 인덴트 기능이 조금 부족한 것 같고, 마크다운은 지금 보니 %s 같은 format code를 문자열과 같은 색으로 처리하는 것 같다. 