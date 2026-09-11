# Count Three-Digit Even Numbers

Given an array of digits, return the number of **distinct three-digit even
numbers** that can be formed using the digits in the array. Each digit may be
used at most once, and the first digit of the number cannot be zero.

## Examples

### Example 1

```text
Input: digits = [2, 1, 3, 0]
Output: 10
Explanation: The 10 valid numbers are 102, 120, 130, 132, 210, 230,
              302, 310, 312, and 320.
```

### Example 2

```text
Input: digits = [2, 2, 8, 8, 2]
Output: 7
Explanation: The valid numbers are 222, 228, 282, 288, 822, 828,
             and 882.
```

### Example 3

```text
Input: digits = [3, 7, 5]
Output: 0
Explanation: No three-digit even number can be formed because there is no
             even digit for the last position.
```

### Example 4

```text
Input: digits = [0, 2, 2, 8]
Output: 9
Explanation: The valid numbers are 202, 208, 220, 228, 280, 282, 802,
             820, and 822.
```

## Constraints

- `3 <= digits.length <= 10`
- `0 <= digits[i] <= 9`
- Each digit may be used at most once when forming a number.

## Solution

**Language:** Python3

The algorithm checks every distinct three-digit even number from 100 through
998 against the digit frequencies. A `Counter` tracks how many copies of each
digit are available, so repeated digits are accepted only when enough copies
exist in the input.

- **Time complexity:** `O(900)`
- **Space complexity:** `O(10)`
