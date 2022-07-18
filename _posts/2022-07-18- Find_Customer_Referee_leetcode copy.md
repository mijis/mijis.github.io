---
layout : single
title: "Find Customer Referee"
categories: leet
tag:  [blog, algorithm, ComputerScience, leetcode, sql]
toc: true
---

## **문제**  
<a href="https://leetcode.com/problems/find-customer-referee/"> [Find Customer Referee] </a>

<p>

Write an SQL query to report the names of the customer that are not referred by the customer with id = 2.

Return the result table in any order.

referee_id가 2가 아닌 customer의 이름을 구하여라.


<br><br>

## **풀이**
```
select  name    
from    Customer
where   referee_id <> 2 or referee_id is null
```



<br><br>

## **+**
referee is null은 꼭 필요하다. 