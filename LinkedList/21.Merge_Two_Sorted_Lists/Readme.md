# 21. Merge Two Sorted Lists

## Problem Statement

You are given the heads of two sorted linked lists `list1` and `list2`.
Merge both lists into a single sorted linked list by splicing together the existing nodes.
Return the head of the merged linked list.

## Example

Input:
list1 = [1,2,4]  
list2 = [1,3,4]

Output:
[1,1,2,3,4,4]

## Approach

Both linked lists are already sorted, so we compare their current nodes one by one.

At each step:
- Pick the node with the smaller value
- Attach it to the result list
- Move forward in that list

This solution uses recursion:
- The smaller node becomes the head
- Its `next` points to the merged result of remaining nodes

Base cases handle empty lists.


## Algorithm

1. If `list1` is null, return `list2`
2. If `list2` is null, return `list1`
3. Compare `list1.val` and `list2.val`
4. If `list1.val <= list2.val`:
   - Set `list1.next` to recursive merge of `list1.next` and `list2`
   - Return `list1`
5. Else:
   - Set `list2.next` to recursive merge of `list1` and `list2.next`
   - Return `list2`
6. Continue until both lists are fully merged

## Time Complexity

O(n + m)  
where n and m are the lengths of the two linked lists

## Notes

- No extra list created
- Nodes are reused (in-place merge)
- Clean and readable recursive solution
