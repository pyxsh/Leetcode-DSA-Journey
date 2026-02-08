# 34. Find First and Last Position of Element in Sorted Array

You are given a sorted array `nums` in non-decreasing order and an integer `target`.

Your task is to find the **starting index** and **ending index** of `target` in the array.
If the target does not exist, return `[-1, -1]`.

You must solve this problem in **O(log n)** time complexity.

## Example

Input:  
nums = [5,7,7,8,8,10], target = 8  

Output:  
[3, 4]

## Approach

Since the array is already sorted, **Binary Search** is the optimal choice.
Instead of searching once, we do **two binary searches**:

1. Find the **first index where value >= target**
2. Find the **first index where value > target**

## Algorithm

1. Store the array and its length.
2. If array is empty, return [-1, -1].
3. Use binary search to find the first index where `nums[mid] >= target`.
   - If not found or value is not equal to target, return [-1, -1].
4. Use binary search to find the first index where `nums[mid] > target`.
5. If the second index exists, last position = index - 1.
   Otherwise, last position = n - 1.
6. Return `[firstIndex, lastIndex]`.

## Code Explanation

The helper function `findFirstTrue()` performs binary search based on a condition:

- `nums[mid] >= target` → for first occurrence
- `nums[mid] > target` → for after last occurrence

Binary search is adjusted by shrinking the right boundary when condition is true.

## Time Complexity

O(log n)
