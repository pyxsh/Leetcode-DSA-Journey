# 88. Merge Sorted Array

You are given two integer arrays nums1 and nums2, both sorted in non-decreasing order.

- nums1 has size m + n
- First m elements of nums1 are valid
- Last n elements of nums1 are 0 (extra space)
- nums2 has n elements

**Task:**

Merge nums2 into nums1 so that nums1 becomes a single sorted array.
Do not return anything, modify nums1 in-place.

## Example

Input:
nums1 = [1,2,3,0,0,0], m = 3  
nums2 = [2,5,6], n = 3  

Output:
[1,2,2,3,5,6]

## Constraints

- 0 <= m, n <= 200
- nums1.length == m + n
- nums2.length == n
- Arrays are already sorted

## Algorithm

1. Loop through nums2 array.
2. nums2 ke elements ko nums1 ke end me copy karo (index m se start).
3. nums1 ko Arrays.sort() se sort kar do.
4. nums1 automatically sorted ho jaayega.

## Time Complexity

O((m + n) log (m + n))
