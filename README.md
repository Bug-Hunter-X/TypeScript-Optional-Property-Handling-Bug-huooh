# TypeScript Optional Property Handling Bug

This repository demonstrates a common, yet subtle, bug in TypeScript related to how optional properties are handled. The `printCoord` function is designed to take a coordinate object with `x` and `y` properties. However, it fails if either `x` or `y` is missing.  The solution demonstrates how to handle optional properties gracefully.

## Bug Description
The original `bug.ts` file contains a function that expects an object with both `x` and `y` properties.  If you pass an object missing either property, the code will throw an error at runtime because the compiler doesn't catch this potential issue without proper type definition adjustments.

## Solution
The `bugSolution.ts` file shows the corrected version.  It uses optional properties (`?`) to indicate that `x` and `y` are optional and handles the case where they are not provided.