# 23. Merge k Sorted Lists

You are given an array of k linked lists.  
Each linked list is sorted in ascending order.

Your task is to merge all these linked lists into one single sorted linked list and return its head.

## Example 1

Input:
lists = [[1,4,5],[1,3,4],[2,6]]

Output:
[1,1,2,3,4,4,5,6]

**Explanation:**

The linked lists are:
1 -> 4 -> 5  
1 -> 3 -> 4  
2 -> 6  

After merging:
1 -> 1 -> 2 -> 3 -> 4 -> 4 -> 5 -> 6

## Example 2

Input:
lists = []

Output:
[]

## Example 3

Input:
lists = [[]]

Output:
[]

## Constraints

k == lists.length  
0 <= k <= 10^4  
0 <= lists[i].length <= 500  
-10^4 <= lists[i] [j] <= 10^4  
Each linked list is sorted in ascending order  
Sum of all nodes will not exceed 10^4  

## Approach

First, traverse all the linked lists and collect every node value into an ArrayList.  
Then sort the ArrayList.  
After sorting, create a new linked list using the sorted values.

## Algorithm

1. Create an empty ArrayList to store node values  
2. Traverse each linked list  
3. Add each node value into the ArrayList  
4. Sort the ArrayList  
5. Create a new linked list from sorted values  
6. Return the head of the new linked list  

## Time and Space Complexity

Time Complexity: O(N log N)  
