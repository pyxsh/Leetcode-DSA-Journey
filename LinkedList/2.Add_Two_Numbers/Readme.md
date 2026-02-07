# 2. Add Two Numbers 

## Problem Statement

You are given two non-empty linked lists representing two non-negative integers.  
The digits are stored in reverse order and each node contains a single digit.

Add the two numbers and return the result as a linked list.

You can assume:
- No leading zeros (except number 0 itself)
- Length of each list is between 1 and 100
- Node values are from 0 to 9

## Examples

Input:
l1 = [2,4,3]  
l2 = [5,6,4]

Output:
[7,0,8]

**Explanation:**
342 + 465 = 807

## Approach

Since digits are stored in reverse order, we can start adding from the head nodes directly.

We:
- Add corresponding digits from both lists
- Keep track of carry
- Create a new node for each digit of the sum
- Continue until both lists and carry are finished

This solution uses recursion to move forward in both linked lists while passing the carry.

## Algorithm

1. Create a recursive helper function that takes:
   - current node of l1
   - current node of l2
   - carry value

2. Base condition:
   - If l1, l2 are null and carry is 0, return null

3. Read current values:
   - If l1 exists, take its value, else 0
   - If l2 exists, take its value, else 0

4. Compute:
   - sum = value1 + value2 + carry
   - new digit = sum % 10
   - new carry = sum / 10

5. Recursively call the function for next nodes with updated carry

6. Create a new ListNode with:
   - calculated digit
   - next pointer from recursive call

7. Return the created node

8. Initial call starts with carry = 0

## Time Complexity

O(max(n, m))  
where n and m are the lengths of the two linked lists

## Notes

- No list reversal needed
- Clean handling of carry
- Works for different length lists
- Final carry is automatically handled
