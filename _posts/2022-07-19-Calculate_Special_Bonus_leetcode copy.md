---
layout : single
title: "Calculate Special Bonus"
categories: leet
tag:  [blog, algorithm, ComputerScience, leetcode, sql]
toc: true
---

## **문제**  
<a href="https://leetcode.com/problems/calculate-special-bonus/"> [Calculate Special Bonus] </a>

<p>

Write an SQL query to calculate the bonus of each employee. The bonus of an employee is 100% of their salary if the ID of the employee is an odd number and the employee name does not start with the character 'M'. The bonus of an employee is 0 otherwise.

Return the result table ordered by employee_id.

각 직원의 보너스를 계산하여라. ID가 홀수이고, 이름이 M으로 시작하지 않을 때 보너스는 salary의 100%이고 아니라면 0이다. 


<br><br>

## **풀이**
1 번 째 풀이 : Runtime: 1372 ms
```
SELECT  employee_id,
CASE
    WHEN MOD(employee_id, 2)=1 AND name NOT LIKE 'M%' THEN salary
    ELSE 0 END AS bonus
FROM        Employees
ORDER BY    employee_id;
``` 
<br><br>


2 번 째 풀이 : Runtime: 718 ms
```
SELECT  employee_id,
(CASE
    WHEN MOD(employee_id, 2)=1 AND name NOT LIKE 'M%' THEN salary
    ELSE 0 END) AS bonus
FROM        Employees
ORDER BY    employee_id;
```

<br><br>

## **+**
1. order by를 놓쳐 실패를 한 번 했었다. 
2. ()의 차이로 runtime이 무척 차이나는 걸 알 수 있다. <br>
    why?!