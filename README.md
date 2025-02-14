# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React's `useEffect` hook: an infinite loop caused by an incorrectly specified dependency array.

The `bug.js` file shows the buggy code.  The `bugSolution.js` file provides the corrected code.

## Bug Description

The original code caused an infinite loop because the `useEffect` hook was not correctly specifying its dependencies. Any change to the component would trigger re-renders, causing the `useEffect` to run again and again.

## Solution

The solution addresses this issue by:

1.  Using the functional update form of `setCount` which prevents unexpected behavior.
2. Correctly listing `count` in the dependency array.  This ensures that the effect only runs when the count changes, breaking the infinite render loop.
