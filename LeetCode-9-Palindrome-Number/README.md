# LeetCode 9 – Palindrome Number

## Problem

Given an integer `num`, determine whether it is a palindrome number.

A palindrome number reads the same from left to right and right to left.

### Examples

```text
121  → Palindrome
123  → Not a Palindrome
1221 → Palindrome
```

## Approach

We can solve this without using strings or built-in functions.

1. Store the original number.
2. Extract the last digit using `% 10`.
3. Add the digit to the reversed number.
4. Remove the last digit using `// 10`.
5. Repeat until `num` becomes `0`.
6. Compare the original number with the reversed number.

## Python Code

```python
num = int(input("Enter a number: "))

original = num

reverse = 0

while num > 0:

    digit = num % 10

    reverse = reverse * 10 + digit

    num = num // 10

if original == reverse:

    print("Palindrome")

else:

    print("Not a Palindrome")
```

## Execution Flow

For `121`:

```text
num = 121
original = 121
reverse = 0

121 → digit 1 → reverse 1 → num 12
12  → digit 2 → reverse 12 → num 1
1   → digit 1 → reverse 121 → num 0
```

Now the loop stops because `num == 0`.

```text
original = 121
reverse  = 121
```

Since they are equal, the output is:

```text
Palindrome
```

## Important Operators

- `% 10` → gets the last digit
- `// 10` → removes the last digit
- `reverse * 10 + digit` → builds the reversed number

## Why `original` is needed

`num` is updated inside the loop:

```text
121 → 12 → 1 → 0
```

So `original` keeps the initial value for the final comparison.

```text
original → 121
num      → 121 → 12 → 1 → 0
reverse  → 0 → 1 → 12 → 121
```

## Complexity

- **Time:** `O(log n)` — one iteration per digit.
- **Space:** `O(1)` — only a fixed number of variables are used.

## Key Learning

This problem teaches number manipulation using arithmetic instead of strings. The same technique is useful for Reverse Integer, Sum of Digits, Count Digits, and Armstrong Number.

**LeetCode:** #9 – Palindrome Number  
**Topic:** Math / Number Manipulation  
**Difficulty:** Easy
