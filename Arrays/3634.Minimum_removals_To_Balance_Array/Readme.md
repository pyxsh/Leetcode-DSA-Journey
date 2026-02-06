# 3634. Minimum Removals to Balance Array

## Problem Statement

You are given an integer array `nums` and an integer `k`.

An array is considered **balanced** if the value of its maximum element is at most `k` times the minimum element.

You may remove any number of elements from `nums` without making it empty.

Return the **minimum number of elements** to remove so that the remaining array is balanced.

Note: An array of size 1 is considered balanced.

## Examples

Example 1:

Input: nums = [2,1,5], k = 2  
Output: 1

**Explanation:** 
Remove `5` to get `[2,1]`.  
Now max = 2, min = 1, and 2 <= 1 * 2. Answer = 1.

Example 2:

Input: nums = [1,6,2,9], k = 3  
Output: 2

**Explanation:**  
Remove `1` and `9` to get `[6,2]`.  
Now max = 6, min = 2, 6 <= 2 * 3. Answer = 2.

Example 3:

Input: nums = [4,6], k = 2  
Output: 0

**Explanation:**  
Array is already balanced. No removals needed.

## Approach

- Sort the array first.  
- Use a **sliding window or binary search** to find the largest subarray where `max <= min * k`.  
- The minimum removals = total elements - size of this subarray.  
- This ensures that after removing elements outside the subarray, the remaining array is balanced.

## Algorithm (Step by Step)

1. Sort `nums`.  
2. Initialize `cnt = 0` to store the size of the largest valid subarray.  
3. Loop over each index `i` in `nums`:
   - Find `j` such that all elements from `i` to `j-1` satisfy `nums[j-1] <= nums[i] * k`.  
   - Use `binarySearch` to efficiently find `j`.  
   - Update `cnt = max(cnt, j - i)`.  
4. Minimum removals = `n - cnt`, where `n` = nums.length.  
5. Return the result.



