---
layout : single
title: "Customers Who Never Order"
categories: leet
tag:  [blog, algorithm, ComputerScience, leetcode]
toc: true
---

## **문제**  
<a href="https://leetcode.com/problems/customers-who-never-order/"> [Customers Who Never Order] </a>

<p>

Write an SQL query to report all customers who never order anything.

Return the result table in any order.

한 버도 주만한 적 없는 고객을 모두 구하여라. 


<br><br>

## **풀이**
```
SELECT      name Customers
FROM        Customers c  
LEFT JOIN   Orders o on o.customerId = c.id
WHERE       o.customerId is null;
``` 



<br><br>

## **+**
inner join과 outer join에 대해 다시 복습해보는 시간이었다. outer join에서 