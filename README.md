# Unexpected Null Behavior in Addition Function

This repository demonstrates a subtle bug related to null handling in a simple JavaScript addition function. The function `foo` is intended to add two numbers, but it unexpectedly returns `null` if either input is `null`.  This behavior might be unexpected if you assume JavaScript's loose typing would automatically coerce `null` to 0.

The `bug.js` file contains the buggy code. The `bugSolution.js` file provides a corrected version.

## Bug
The issue lies in the strict equality check (`===`) within the `if` condition. This check doesn't perform type coercion, so `null` is not treated as 0 in this case. To fix this, the function should explicitly check for and handle `null` values, ideally by converting them to 0.