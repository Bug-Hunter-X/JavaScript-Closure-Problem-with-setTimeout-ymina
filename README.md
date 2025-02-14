# JavaScript Closure Problem with setTimeout

This repository demonstrates a common issue with closures in JavaScript when using `setTimeout` within a loop. The problem arises because the `setTimeout` callback function does not capture the value of `i` at the time it's set, but rather when it's executed.  This results in all callbacks logging the final value of `i` (which is 10). 

The `bug.js` file contains the buggy code.  The `bugSolution.js` file shows the corrected version.

## Solution

The solution involves using an immediately invoked function expression (IIFE) or `let` to create a new scope for each iteration of the loop, thereby capturing the correct value of `i` for each callback.