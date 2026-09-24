# 242. Valid Anagram

**Difficulty:** Easy  
**Language:** Python  
**Topic:** String / Sorting

## Problem

Given two strings `s` and `t`, return `True` if `t` is an anagram of `s`, and `False` otherwise.

An **anagram** is a word or phrase formed by rearranging all the characters of another word or phrase, using every character the same number of times.

### Example 1

**Input:**
```
s = "anagram"
t = "nagaram"
```

**Output:**
```
True
```

### Example 2

**Input:**
```
s = "rat"
t = "car"
```

**Output:**
```
False
```

## Approach

First, compare the lengths of the two strings.

- If their lengths are different, they cannot be anagrams.
- If their lengths are equal, sort both strings and compare them.

For example:

```
s = "anagram"
t = "nagaram"

sorted(s) = ['a', 'a', 'a', 'g', 'm', 'n', 'r']
sorted(t) = ['a', 'a', 'a', 'g', 'm', 'n', 'r']
```

Since the sorted strings are equal, the strings are anagrams.

## Key Concept

The `sorted()` function returns the characters of a string in sorted order.

```python
sorted("cab")
# ['a', 'b', 'c']
```

So two strings are anagrams when their sorted character lists are equal.

## Solution

```python
class Solution:
    def isAnagram(self, s: str, t: str) -> bool:
        if len(s) != len(t):
            return False

        return sorted(s) == sorted(t)
```

## Complexity

- **Time:** O(n log n) — both strings are sorted.
- **Space:** O(n) — the sorted character lists require additional space.

---

**LeetCode:** 242 - Valid Anagram  
**Status:** Accepted ✅
