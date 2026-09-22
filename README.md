# LeetCode 224 - Basic Calculator

## Problem

Given a string `s` representing a valid mathematical expression, implement a basic calculator to evaluate the expression.

The expression can contain:

* Digits
* `+`
* `-`
* `(`
* `)`
* Spaces

The calculator should return the result of the expression.

## Example

### Input

```text
s = "1 + 1"
```

### Output

```text
2
```

### Example 2

```text
s = " 2-1 + 2 "
```

Output:

```text
3
```

### Example 3

```text
s = "(1+(4+5+2)-3)+(6+8)"
```

Output:

```text
23
```

## Approach

This solution uses a stack to handle parentheses.

We maintain:

* `result` - current calculated result
* `number` - current number being formed
* `sign` - current sign (`+1` or `-1`)
* `stack` - stores the result and sign before entering parentheses

When we encounter:

* A digit → build the number.
* `+` → add the previous number and set the sign to positive.
* `-` → add the previous number and set the sign to negative.
* `(` → save the current result and sign in the stack.
* `)` → finish the current expression and combine it with the values stored before the parentheses.

## Algorithm

1. Initialize `result`, `number`, and `sign`.
2. Traverse the string character by character.
3. Build numbers when digits are encountered.
4. Apply the previous sign when `+` or `-` is found.
5. Store the current result and sign when `(` is encountered.
6. Restore them when `)` is encountered.
7. Add the final number to the result.
8. Return the result.

## Complexity

* Time Complexity: `O(n)`
* Space Complexity: `O(n)`

Where `n` is the length of the input string.

## Language

Python

## LeetCode

Problem: 224 - Basic Calculator

## Author

**T.Nandhini**
