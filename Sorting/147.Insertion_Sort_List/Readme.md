## 147. Insertion Sort List

You are given the head of a singly linked list. Sort the list using Insertion Sort and return the head of the sorted list.

Insertion Sort works by taking one element at a time from the input list and inserting it into its correct position in the sorted part of the list.

## Example 1

Input:  head = [4,2,1,3]
Output: [1,2,3,4]

## Example 2

Input:  head = [-1,5,3,4,0]
Output: [-1,0,3,4,5]

## Constraints

- 1 <= number of nodes <= 5000
- -5000 <= Node.val <= 5000

## Approach

First, traverse the linked list and store all node values in an ArrayList.
Then sort the ArrayList using built-in sorting.
After sorting, traverse the linked list again and overwrite each node’s value using the sorted values from the ArrayList.

## Algorithm

1. Create an empty ArrayList
2. Traverse the linked list and store node values in the list
3. Sort the ArrayList
4. Traverse the linked list again and replace node values
5. Return the head of the list

## Time and Space Complexity

- Time Complexity: O(n log n)
- Space Complexity: O(n)
