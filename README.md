# React useEffect Hook Dependency Array Error

This repository demonstrates a common error in React's `useEffect` hook: forgetting to include state variables in the dependency array. This can lead to unexpected behavior due to stale closures.

## Bug Description

The `bug.js` file contains a `MyComponent` that uses the `useState` and `useEffect` hooks. The `useEffect` hook is intended to log the current count to the console after each click. However, because the `count` variable is missing from the dependency array, the effect only runs once during the initial render.  Subsequent clicks will not update the logged count.

## Solution

The `bugSolution.js` file demonstrates the correct approach.  By including `count` in the dependency array, the effect will now run every time the `count` value changes, leading to correct logging of the count.