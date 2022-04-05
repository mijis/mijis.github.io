---
layout : single
title: "recompiling"
categories: CS50
tag: [CS50, blog, ComputerScience]
toc: true
---

> ## **수업내용**

**Q. 질문**<br>
1. 프로그램을 수정하고, 또 다시 수정해서 실행한다면 그 변화는 반영이 되는가? <br>
rm hello 를 쳐서 hello 파일을 삭제하면 hello.c 파일은 그대로 남아있다. 그러나 ./hello 하여 hello 를 실행하려 하면 No such file or directory라고 나온다. 다시 make hello를 한 후 ls해보면 하이라이트 표시된 hello* 와 hello.c가 나온다. 하이라이트 표시된 hello* 는 실행가능하다는 뜻으로 쉽게 표현하자면 클릭 가능하다는 말이다. 이제 ./hello해보면 hello의 결과가 나온다. <br>

2. 이제 hello 파일에서 내용을 수정, 저장 후 ./hello 해보면 여전히 예전의 내용이 나온다. 그 이유는 무엇인가?<br>
컴파일이 되지 않았기 때문이다. make hello가 다시 필요하다는 뜻이다. 그럼 새로 저장된 내용이 나온다. 그렇다고 해서 컴파일 된 hello.c 파일이 여러 개 저장되는 것은 아니다. 예전의 파일에 덮어쓰여진다. <br>

3. 만약 ./hello.c하면 어떻게 되는가?<br>
permission design이라고 나온다. 실행 권한이 없다는 뜻이다. 
<br><br>

<div>

> ## **소감**
이클립스를 사용하면서 컴파일은 자동으로 되게 해서 사용을 하다보니 이렇게 컴파일이 따로 들어가는 게 생소하지만, 더 차근차근 알아가는 것 같아 좋다.

</div>