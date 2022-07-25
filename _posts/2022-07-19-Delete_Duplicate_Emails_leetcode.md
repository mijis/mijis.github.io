---
layout : single
title: "Delete Duplicate Emails"
categories: leet
tag:  [blog, algorithm, ComputerScience, leetcode, sql]
toc: true
---

## **문제**  
<a href="https://leetcode.com/problems/delete-duplicate-emails/"> [Delete Duplicate Emails] </a>

<p>

Write an SQL query to delete all the duplicate emails, keeping only one unique email with the smallest id. Note that you are supposed to write a DELETE statement and not a SELECT one.


작은 아이디의 메일만 남겨두고 중복 메일을 삭제해라. delete 문만 사용하고, select문을 사용하지 말라. 


<br><br>

## **풀이**
1 번 째 풀이 : Runtime: 617 ms
```
update
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