# 268. Missing Number

You are given an array `nums` containing `n` distinct numbers taken from the range `[0, n]`.
Your task is to find the one number that is missing from the array.

## Examples

Input:
nums = [3,0,1]  
Output:
2  

**Explanation:**
Range is [0,3]. Number 2 is missing.

Input:
nums = [0,1]  
Output:
2  

Input:
nums = [9,6,4,2,3,5,7,0,1]  
Output:
8  

## Constraints

- 1 <= nums.length <= 10^4
- 0 <= nums[i] <= n
- All numbers are unique

## Approach

Since the numbers should ideally be in the range `0` to `n`,
after sorting the array, each index should contain the same value as the index.

If at any index `i`, `nums[i] != i`, then `i` is the missing number.
If all values match their indices, then the missing number is `n`.

## Algorithm

1. Sort the array
2. Traverse from index `0` to `n-1`
3. If `nums[i] != i`, return `i`
4. If loop completes, return `n`
