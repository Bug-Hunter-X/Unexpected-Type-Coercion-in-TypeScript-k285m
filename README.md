# Unexpected Type Coercion in TypeScript

This repository demonstrates a common error in TypeScript where type coercion can lead to unexpected behavior at runtime. The `add` function is declared to accept only numbers, but because TypeScript allows type coercion in some cases, passing a string doesn't trigger a compile-time error.  This results in string concatenation instead of numeric addition.

## How to Reproduce

1. Clone this repository.
2. Run `tsc bug.ts` to compile the code.
3. Run the compiled JavaScript file (e.g., `node bug.js`).

You'll observe that the output is "12" instead of the expected "3".

## Solution

The solution involves stricter type checking to prevent this coercion. The improved version is available in `bugSolution.ts`.