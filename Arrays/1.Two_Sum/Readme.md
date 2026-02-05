# Two Sum (LeetCode 1)

## Problem
Given an array of integers `nums` and a `target` number.  
Find the indices of two different numbers in the array such that their sum equals the target.

Each input has exactly one valid answer, and you cannot use the same element twice.

## Input
- `nums`: integer array
- `target`: integer

## Output
- An array of two indices where the values sum up to target

## Examples
1. Input: nums = [2,7,11,15], target = 9  
   Output: [0,1]  
   Explanation: nums[0] + nums[1] = 2 + 7 = 9

2. Input: nums = [3,2,4], target = 6  
   Output: [1,2]

3. Input: nums = [3,3], target = 6  
   Output: [0,1]

## Brute Force (Hinglish)
Isme hum array ke har element ke saath baaki elements ka sum check karte hain using two loops.  
Jaise hi correct pair milta hai, indices return kar dete hain.

## Complexity
- Time: O(n²)
- Space: O(1)
