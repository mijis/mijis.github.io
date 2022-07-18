---
layout : single
title: "Recyclable and Low Fat Products"
categories: leet
tag:  [blog, algorithm, ComputerScience, leetcode, sql]
toc: true
---

## **문제**  
<a href="https://leetcode.com/problems/recyclable-and-low-fat-products/"> [Leetcode Recyclable and Low Fat Products] </a>
<p>

Write an SQL query to find the ids of products that are both low fat and recyclable.<br>
Return the result table in any order.

low_fat이 'Y'이고 recylclable이 'Y'인 product_ids를 구하여라. 



<br><br>

## **풀이**
```
SELECT  product_id 
FROM    Products
WHERE   low_fats = 'Y' and recyclable = 'Y';
```


<br><br>

## **+**
Oracle에서는 enum의 값이 없어 low fat과 recyclable의 값을 문자열로 생각하고 풀었다. 

<br><br>

## **enum이란**
enum 타입은 캐릭터형 타입으로 지정한 타입만 넣을 수 있게 해주는 기능이다. null이나 empty string을 넣을 수 있고, null이나 empty string이 들어간 값은 유효하지 않은 값이 된다. 또 하나의 중요한 점은 index를 사용할 수 있다는 점이다. index는 1로 시작되며 0은 유효하지 않은 값으로 분류된다. 