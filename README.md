# Move Zeroes

## Problem
Given an integer array `nums`, move all 0's to the end while maintaining the relative order of non-zero elements.  
Do this in-place.

---

## Approach
- Use two pointers:
  - `i` → position to place next non-zero
  - `j` → scans the array
- If `nums[j] != 0`, swap `nums[i]` and `nums[j]`, then increment `i`

---

## Complexity
- Time: O(n)
- Space: O(1)

---

## Key Insight
Swapping keeps the order of non-zero elements and moves zeros to the end without extra space.

---

## Example
Input: [0,1,0,3,12]  
Output: [1,3,12,0,0]

---

## Code
```python
def moveZeroes(nums):
    i = 0
    for j in range(len(nums)):
        if nums[j] != 0:
            nums[i], nums[j] = nums[j], nums[i]
            i += 1
