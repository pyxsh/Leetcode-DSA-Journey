# Pascal's Triangle (LeetCode 118)

## Problem Statement
Given an integer `numRows`, return the first `numRows` rows of **Pascal's Triangle**.

In Pascal's Triangle:
- Each row starts and ends with `1`
- Every middle element is the sum of the two numbers directly above it
- Row indexing starts from `0`


## Examples

### Example 1
**Input**
```
numRows = 5
```

**Output**
```
[
 [1],
 [1,1],
 [1,2,1],
 [1,3,3,1],
 [1,4,6,4,1]
]
```

### Example 2
**Input**
```
numRows = 1
```

**Output**
```
[[1]]
```

## Core Idea
Instead of using previous rows to calculate the next row, this solution uses a **mathematical approach** based on **Binomial Coefficients**.

Formula used:
```
C(n, k) = C(n, k-1) * (n - k + 1) / k
```

This avoids:
- Factorials ❌
- Extra space ❌
- Complex logic ❌

Result:
- Faster
- Cleaner
- Interview-friendly


## Approach (Code-Oriented Explanation)

1. Create a list `res` to store all rows.
2. Loop from row `0` to `numRows - 1`.
3. For each row:
   - Add the first element `1`.
   - Use a variable `val` to calculate next values using the formula.
4. Add each completed row to the result list.
5. Return the final Pascal’s Triangle.

## 🧠 Algorithm

1. Initialize an empty list `result`.

2. Loop `n` from 0 to `numRows - 1`:
   2.1 Create a new list `row`.
   2.2 Add `1` as the first element of the row.
   2.3 Initialize `val = 1`.

   2.4 Loop `k` from 1 to `n`:
       - Update `val = val * (n - k + 1) / k`.
       - Add `val` to the current row.

   2.5 Add the completed `row` to `result`.

3. Return the `result` list.


## Complexity Analysis
- **Time Complexity:** `O(n²)`
- **Space Complexity:** `O(n²)` (output storage)

---

## Summary
- Problem Type: **Array / Math**
- Difficulty: **Easy**
- Technique Used: **Binomial Coefficient**
- Status: **Accepted**
