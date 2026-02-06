# 3637. Trionic Array I

## Problem Statement

You are given an integer array `nums` of length `n`.

An array is called trionic if there exist indices `p` and `q` such that:

- 0 < p < q < n - 1
- nums[0 ... p] is strictly increasing
- nums[p ... q] is strictly decreasing
- nums[q ... n - 1] is strictly increasing

Return true if the array is trionic, otherwise return false.

## Examples

Example 1:

Input:
nums = [1,3,5,4,2,6]

Output:
true

**Explanation:**
nums[0...2] = [1,3,5] is strictly increasing  
nums[2...4] = [5,4,2] is strictly decreasing  
nums[4...5] = [2,6] is strictly increasing  

Example 2:

Input:
nums = [2,1,3]

Output:
false

**Explanation:**
It is not possible to split the array into the required three parts.

## Approach

The array must follow a strict pattern:
increasing first, then decreasing, and then increasing again.

We traverse the array using pointers and validate each segment one by one.
No extra data structure is used.

**Steps followed:**

- First, move forward while elements are strictly increasing.
- Then, move forward while elements are strictly decreasing.
- Finally, move forward while elements are strictly increasing again.
- If all three parts exist and the traversal reaches the end, the array is trionic.

## Algorithm

1. Initialize `p = 0`.
2. Move `p` forward while `nums[p] < nums[p + 1]` and `p < n - 2`.
3. If `p == 0`, return false.
4. Set `q = p`.
5. Move `q` forward while `nums[q] > nums[q + 1]`.
6. If `q == p` or `q == n - 1`, return false.
7. Move `q` forward while `nums[q] < nums[q + 1]`.
8. If `q == n - 1`, return true.
9. Otherwise, return false.


