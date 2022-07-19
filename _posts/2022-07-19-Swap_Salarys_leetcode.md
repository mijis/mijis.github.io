---
layout : single
title: "Swap Salary"
categories: leet
tag:  [blog, algorithm, ComputerScience, leetcode, sql]
toc: true
---

## **문제**  
<a href="https://leetcode.com/problems/swap-salary/"> [Swap Salary] </a>

<p>

Write an SQL query to swap all 'f' and 'm' values (i.e., change all 'f' values to 'm' and vice versa) with a single update statement and no intermediate temporary tables.

Note that you must write a single update statement, do not write any select statement for this problem.

f와 m의 값을 서로 바꿔라. 하나의 update 쿼리를 쓰고, select문을 쓰지 말라.


<br><br>

## **풀이**
1 번 째 풀이 : Runtime: 617 ms
```
update  Salary
set   sex = (case when sex='m' then 'f' 
                 when sex='f' then 'm' end);
``` 
<br><br>


2 번 째 풀이 : Runtime: 513 ms
```
update  Salary
set   sex = (case when sex='m' then 'f' else 'm' end);
```

<br><br>

## **+**
1. 바보 같게도 else를 쓰지 않은 이상한 풀이를 냈다.