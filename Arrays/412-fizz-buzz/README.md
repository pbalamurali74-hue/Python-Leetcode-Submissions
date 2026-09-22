# 412. Fizz Buzz

**Difficulty:** Easy  
**Language:** Python  
**Topic:** Array / Loops / Modulo

## Problem

Given an integer `n`, return a list of strings from `1` to `n`.

- Multiples of 3 → `"Fizz"`
- Multiples of 5 → `"Buzz"`
- Multiples of both 3 and 5 → `"FizzBuzz"`
- Otherwise → the number as a string

### Example

**Input:**
```
n = 5
```

**Output:**
```
["1", "2", "Fizz", "4", "Buzz"]
```

## Approach

Create an empty result list and loop from `1` to `n`.

For every number, check the conditions in this order:

1. Divisible by both 3 and 5 → `FizzBuzz`
2. Divisible by 3 → `Fizz`
3. Divisible by 5 → `Buzz`
4. Otherwise → add the number as a string

The **FizzBuzz condition must come first**, because a number such as 15 is divisible by both 3 and 5.

## Key Concept

The modulo operator `%` gives the remainder.

```python
i % 3 == 0
```

means `i` is exactly divisible by 3.

## Complexity

- **Time:** O(n) — each number is checked once.
- **Space:** O(n) — the result list stores n values.

## Solution

See [solution.py](./solution.py).

---

**Status:** Accepted ✅
