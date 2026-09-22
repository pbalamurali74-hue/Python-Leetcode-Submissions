# 1929. Concatenation of Array

**Difficulty:** Easy  
**Language:** Python  
**Topic:** Array

## Problem
Given an integer array `nums`, create an array containing `nums` followed by another copy of `nums`.

### Example
`nums = [1, 2, 1]` → `[1, 2, 1, 1, 2, 1]`

## Approach
Use Python list concatenation:

```python
answer = nums + nums
```

The code then converts the result to a list and returns it.

## Complexity
- **Time:** O(n)
- **Space:** O(n) for the output array

## Key Concept
List concatenation using `+`.

## Solution
[View solution.py](./solution.py)

**Status:** Completed
