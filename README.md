# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common issue in JavaScript related to closures and the `setTimeout` function within loops. The problem arises because the callback function inside `setTimeout` does not capture the value of `i` at the time it's created, but rather captures a reference to the variable `i` itself.  This means that when the `setTimeout` callbacks finally execute, the value of `i` might have already changed.

The `bug.js` file contains the buggy code. The `bugSolution.js` file shows how to correctly capture the value of `i` using an immediately invoked function expression (IIFE).