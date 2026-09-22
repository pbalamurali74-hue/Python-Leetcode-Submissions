# 1480. Running Sum of 1d Array

**Difficulty:** Easy  
**Language:** Python  
**Topic:** Array / Prefix Sum

## Problem

Given an array `nums`, return the running sum of the array.

The running sum at index `i` is:

`nums[0] + nums[1] + ... + nums[i]`

### Example

**Input:**
```
[1, 2, 3, 4]
```

**Output:**
```
[1, 3, 6, 10]
```

## Approach

Start from the second element (index 1).

For every element:

```python
nums[i] += nums[i - 1]
```

This adds the previous running sum to the current value.

For example:

```text
[1, 2, 3, 4]

i = 1 → 2 + 1 = 3
i = 2 → 3 + 3 = 6
i = 3 → 4 + 6 = 10

Result → [1, 3, 6, 10]
```

## Why This Works

After updating `nums[i]`, the element at index `i` contains the sum of all elements from index 0 to `i`.

So the array itself stores the running sums, and we don't need another array.

## Complexity

- **Time:** O(n) — we visit each element once.
- **Space:** O(1) — no extra array is created.

## Key Concept

**Prefix Sum / Running Sum**

The important idea is to reuse the result calculated at the previous index instead of calculating the sum from the beginning every time.

## Solution

See [solution.py](./solution.py).

---

**Status:** Accepted ✅
