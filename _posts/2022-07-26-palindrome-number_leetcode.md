---
layout : single
title: "palindrome-number"
categories: leet
tag:  [blog, algorithm, ComputerScience, leetcode]
toc: true
---

## **문제**   
[Leetcode palindrome-number] (https://leetcode.com/problems/palindrome-number/)
<p>

Given an integer x, return true if x is palindrome integer.
An integer is a palindrome when it reads the same backward as forward.
For example, 121 is a palindrome while 123 is not.

정수 x가 주어지고, x가 회문(거꾸로 읽어도 같은 숫자)이면 true를 반환하라. 
거꾸로 읽어도 똑같이 읽을 수 있다면, palindrome(회문) 정수라고 할 수 있다.
예시로, 121은 회문이고 123은 회문이 아니다. ds

</p>
<br>

## **풀이**
```java
class Solution {
    public boolean isPalindrome(int x) {
        
        String number = String.valueOf(x);
        int length = number.length(); 
        int cnt = 0;
        
        for(int i=0; i<(length/2); i++){
            cnt = number.charAt(i) == number.charAt(length-i-1)? cnt+1:cnt;
        }    
        
        return cnt==length/2? true:false;
        
    }    
    
}
```

Runtime: 13 ms

Memory Usage: 46.1 MB


<br><br>

## **후기** 
이 알고리즘은 나에게 꽤 의미가 있는 알고리즘이다. 첫 코딩 테스트 문제가 이것이기도 했고, solution을 보면서 approach하는 사고 방법을 따라가고 싶다고 생각하게 된 계기라 또 더 의미가 깊은 것 같다. 