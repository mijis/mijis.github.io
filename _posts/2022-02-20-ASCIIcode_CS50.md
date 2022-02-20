---
layout : single
title: "Letters"
categories: CS50
tag: [CS50, blog, ComputerScience]
toc: true
---

# ASCII review
<br>

> ## **수업내용**
---
ASCII(American Standard Code for Infromation Interchage)를 배웠다. 65, 66, 67의 숫자는 A, B, C라는 텍스를 의미한다는 것이다. 가령 72  73  33은 "HI!"를 의미하듯이 말이다. 

사람은 아스키코드를 보면서 일일이 비교해야하지만 컴퓨터는 모국어처럼 이를 받아들이도록 디자인되어있다. 그렇지만 컴퓨터가 받아들이는 이진수의 숫자(우리는 십진수로 표현했지만)에는 표준적인 길이가 있는데, 8bit이다. 예를 들어 "HI!" H, 72는 2진수로 01001000이고, I, 73은 01001001이며, !, 33은 00100001이다. 모두 8자리 숫자이다. 여기서 알 수 있듯이, 각각 한 자리수를 bit라고 하고, bit는 무척이나 작은 단위이므로 우리는 8bit를 기준 길이로 잡으며 이를 byte라 한다. 
<br>

#### **1 B(byte) = 8 bits**

<br>
100cm가 1m가 되는 것과 똑같은 원리이다. 결국 "HI!"는 24bits로 무척이나 작은 값이다. 그렇다면 8bit 즉 1byte로 나타낼 수 있는 최대값은 얼마인가! 11111111 즉 255이다. 

여기서 더 나아가면 kilobyte(thousands of byte), megabyte(millions of byte), gigabyte(billions of byte), terrabyte(trillions of byte)가 있다. 이들을 이용해서 우리는 많은 양의 데이터를 관리할 수 있다.
<br>


### **1 KB(kilobyte) = 2<sup>10** **B(byte)**
### **1 MB(megabyte) = 2<sup>10** **KB(kilobyte) =  2<sup>20** **B(byte)**
### **1 GB(gigabyte) = 2<sup>10** **MB(megabyte) =  2<sup>30** **B(byte)**
### **1 TB(terabyte) = 2<sup>10** **GB(gigabyte) =  2<sup>40** **B(byte)**

 <br><br>

하지만 ASCII code는 0까지 합쳐서 256자리 수 밖에 표현할 수 없다. 영어만 표현하기에는 적합하지만, 알파벳이 아닌 언어들은 어떻게 표현해야하는지에 대한 문제가 남는다. 