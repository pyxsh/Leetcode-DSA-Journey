# 19. Remove Nth Node From End of List

Given the head of a singly linked list, remove the **n-th node from the end** of the list and return its head.

## Examples

Input:  
head = [1,2,3,4,5], n = 2  
Output:  
[1,2,3,5]

Input:  
head = [1], n = 1  
Output:  
[]

Input:  
head = [1,2], n = 1  
Output:  
[1]

## Approach

Instead of doing tricky two-pointer, we take a **simpl3 approach**:

1. Traverse the linked list and store each node in a list.
2. Calculate the index of the node to be removed using:
   
   removeIndex = size - n
3. If the node to be removed is the **head**, simply return `head.next`.
4. Otherwise, update the `next` pointer of the previous node to skip the target node.

## Algorithm

1. Create a list to store nodes.
2. Traverse the linked list and add all nodes to the list.
3. Compute index to remove: `size - n`
4. If index is 0:
   - Remove head and return `head.next`
5. Else:
   - Link previous node to next of the target node
6. Return original head


## Time Complexity

O(n)  
where n is the number of nodes in the linked list

