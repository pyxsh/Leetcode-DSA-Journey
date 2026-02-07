# 203. Remove Linked List Elements

You are given the head of a linked list and an integer `val`.

Remove all nodes from the linked list whose value is equal to `val` and return the new head of the linked list.

If all nodes are removed, return `null`.

## Examples

Input:
head = [1,2,6,3,4,5,6], val = 6  
Output:
[1,2,3,4,5]

Input:
head = [] , val = 1  
Output:
[]

Input:
head = [7,7,7,7], val = 7  
Output:
[]

## Approach

We traverse the linked list and store only those node values which are not equal to `val`.

After traversal:
- If no values are left, return `null`
- Otherwise, create a new linked list using the stored values

This approach avoids complex pointer handling and keeps the logic simple and clear.

## Algorithm

1. Create an empty list to store values
2. Start traversing the linked list from head
3. For each node:
   - If node value is not equal to `val`, store it
4. After traversal:
   - If stored list is empty, return `null`
5. Create a new linked list using the stored values
6. Return the head of the newly created linked list

## Time Complexity

O(n)  
where n is the number of nodes in the linked list

## Notes

- Original list is not modified
- Easy to understand and implement
- Handles empty list and full removal cases properly
