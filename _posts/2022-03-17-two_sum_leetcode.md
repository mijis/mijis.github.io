---
layout : single
title: "Two Sum"
categories: leet
tag:  [blog, algorithm, ComputerScience, leetcode]
toc: true
---

## **문제**   
[Leetcode Two Sum] (https://leetcode.com/problems/two-sum/)
<p>
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

주어진 정수 배열 nums와 정수 target을 이용하여, 배열의 두 숫자의 합이 target이 되는 두 숫자의 인덱스를 반환하라.
</p>
<br>

## **풀이**
```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
                
        for(int i=0; i<nums.length-1; i++) {
            for(int j=i+1; j<nums.length; j++){
                if(nums[i]==target-nums[j]) {
                    return new int[]{i,j};
                }
                
            }
        }   
        return new int[2]; 
    }
}
```

Runtime: 48 ms

Memory Usage: 41.9 MB


<br><br>




## **후기** 
처음 알고리즘을 풀어보는 것이라 엉성하고 시작부터 잘 되지는 않았다. 우여곡절 끝에 풀수는 있었지만, runtime을 줄이고 메모리 용량을 덜 차지하는 방향을 좀 더 생각해봐야겠다.




