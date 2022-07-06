---
layout : single
title: "Big Countries"
categories: leet
tag:  [blog, algorithm, ComputerScience, leetcode]
toc: true
---

## **문제**  
<a href="https://leetcode.com/problems/big-countries/"> [Leetcode big-countries] </a>
<p>

A country is big if: <br>
it has an area of at least three million (i.e., 3000000 km2), or
it has a population of at least twenty-five million (i.e., 25000000).
Write an SQL query to report the name, population, and area of the big countries.<br>
Return the result table in any order.


Big Countries는 area가 3000000 km2 이상이거나, 인구가 25000000 이상이어야한다. Big Countries의 이름, 인구, 인구를 나타내는 SQL문을 작성하라. 
<br><br><br><br>


## **풀이**
```
SELECT  name, population, area  <br>
FROM    World
WHERE   area >= 3000000 OR population >= 25000000;
```