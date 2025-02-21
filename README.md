# JavaScript Type Coercion Bug

This repository demonstrates a subtle bug in JavaScript related to type coercion within conditional statements.  The code appears to correctly handle null and negative numbers, but fails when dealing with strings that can be coerced to numbers.

## Bug Description
The function `foo` intends to return 0 if the input is null, -1 if the input is a negative number, and 1 otherwise. However, due to JavaScript's loose typing and implicit type coercion, a string input such as "0" will be coerced to a number (0) and trigger the `x < 0` condition incorrectly.

## How to Reproduce
1. Clone this repository.
2. Open `bug.js`.
3. Run the code using Node.js or a similar JavaScript environment.
4. Observe the unexpected output for the input '0'.

## Solution
The solution involves adding explicit type checking to avoid implicit coercion.  See `bugSolution.js` for the corrected code.

## Lessons Learned
This highlights the importance of explicit type checking in JavaScript to prevent unexpected behavior caused by implicit type coercion, especially when dealing with user input or data from external sources.