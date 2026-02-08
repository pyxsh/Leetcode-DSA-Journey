# 74. Search a 2D Matrix

You are given an m x n integer matrix.

Properties of the matrix:

- Each row is sorted in non-decreasing order.
- The first element of each row is greater than the last element of the previous row.

Given an integer target, return true if target exists in the matrix, otherwise return false.

## Example

Input:
matrix = [[1,3,5,7],
          [10,11,16,20],
          [23,30,34,60]]
target = 3

Output:
true

Input:
target = 13

Output:
false

## Constraints

- 1 <= m, n <= 100
- -10^4 <= matrix[i][j], target <= 10^4

## Approach

Isme humne simple traversal use kiya hai.

- Har row ko ek-ek karke check karte hain.
- Har row ke andar har element ko check karte hain.
- Jaise hi target milta hai, true return kar dete hain.
- Agar poori matrix traverse kar li aur target nahi mila, to false return kar dete hain.

## Algorithm

1. Loop through each row of the matrix.
2. For each row, loop through each column.
3. If matrix[r][c] == target, return true.
4. If traversal complete ho jaye aur target na mile, return false.

## Time Complexity

O(m * n), because har element check ho raha hai.
