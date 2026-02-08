# 704. Binary Search

You are given a sorted array of integers `nums` in ascending order and an integer `target`.
Your task is to find the index of `target` in the array.

- If `target` exists, return its index
- If `target` does not exist, return `-1`

The solution must run in `O(log n)` time.

## Approach

Since the array is already sorted, we use **Binary Search**.

Binary Search works by repeatedly dividing the search space into half:

- Compare the middle element with the target
- If equal, return the index
- If target is greater, search in the right half
- If target is smaller, search in the left half

This reduces the time complexity from linear to logarithmic.

## Algorithm

1. Initialize two pointers:
   - `left = 0`
   - `right = nums.length - 1`
2. While `left <= right`:
   - Calculate `mid = left + (right - left) / 2`
   - If `nums[mid] == target`, return `mid`
   - If `nums[mid] < target`, move `left` to `mid + 1`
   - Else move `right` to `mid - 1`
3. If the loop ends and target is not found, return `-1`

## Time Complexity

O(log n) because the search space is reduced by half each iteration
