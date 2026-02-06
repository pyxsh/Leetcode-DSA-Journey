# 3640. Trionic Array II

## Problem Statement

You are given an integer array `nums` of length `n`.
A **trionic subarray** is a contiguous subarray `nums[l...r]` (0 <= l < r < n) for which there exist indices `l < p < q < r` such that:
- `nums[l...p]` is strictly increasing  
- `nums[p...q]` is strictly decreasing  
- `nums[q...r]` is strictly increasing  

Return the **maximum sum** of any trionic subarray in `nums`.

## Examples

Example 1:

Input: nums = [0,-2,-1,-3,0,2,-1]  
Output: -4

**Explanation:** 

Pick l = 1, p = 2, q = 3, r = 5  
- nums[1...2] = [-2, -1] is strictly increasing  
- nums[2...3] = [-1, -3] is strictly decreasing  
- nums[3...5] = [-3,0,2] is strictly increasing  
Sum = -2 + -1 + -3 + 0 + 2 = -4

Example 2:

Input: nums = [1,4,2,7]  
Output: 14

**Explanation:**

Pick l = 0, p = 1, q = 2, r = 3  
- nums[0...1] = [1,4] is strictly increasing  
- nums[1...2] = [4,2] is strictly decreasing  
- nums[2...3] = [2,7] is strictly increasing  
Sum = 1 + 4 + 2 + 7 = 14

## Approach

- Traverse the array and look for **increasing → decreasing → increasing** patterns.  
- For each valid trionic subarray, calculate its sum.  
- Keep track of the maximum sum found.  
- Use pointers and partial sums to avoid recomputation.  

## Algorithm (Step by Step)

1. Initialize `i = 0` and `ans = Long.MIN_VALUE`.  
2. Loop while `i < n`:  
   - Set `l = i` and move `i` forward while the sequence is strictly increasing.  
   - If increasing part is too short, continue to next `i`.  
   - Let `p = i - 1`, initialize sum `s` for the increasing-decreasing segment.  
   - Move `i` forward while sequence is strictly decreasing, add to sum.  
   - Check for valid decreasing segment. If invalid, continue.  
   - Let `q = i - 1`, start next increasing part. Add sum of increasing sequence.  
   - Check left side of first increasing segment for extra contribution.  
   - Update `ans = max(ans, s)`.  
   - Move `i` to `q` to continue scanning.  
3. Return `ans` as the maximum sum.

