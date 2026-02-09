# 75. Sort Colors

Given an array `nums` containing only `0`, `1`, and `2`, sort the array **in-place** so that all `0`s come first, followed by `1`s, then `2`s.  
You are **not allowed** to use any built-in sorting function.

## Example

Input:
nums = [2,0,2,1,1,0]

Output:
[0,0,1,1,2,2]

## Approach & Algorithm

We use **three pointers** to solve this in **one pass**:

- `low` → position where next `0` should be placed  
- `mid` → current index being checked  
- `high` → position where next `2` should be placed  

Rules while traversing the array:

- If `nums[mid] == 0`  
  → swap it with `nums[low]`  
  → move both `low` and `mid` forward

- If `nums[mid] == 1`  
  → it's already in correct place  
  → just move `mid` forward

- If `nums[mid] == 2`  
  → swap it with `nums[high]`  
  → move `high` backward  
  → do NOT move `mid` because the swapped element must be checked again

This algorithm is called the **Dutch National Flag Algorithm**.

## Time & Space Complexity

- Time Complexity: O(n)
- Space Complexity: O(1)
