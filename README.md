# React State Update Bug: Direct Mutation in useEffect

This repository demonstrates a common but subtle error in React: directly mutating state within the `useEffect` hook.  This example uses the `useState` hook incorrectly, leading to the counter not updating properly.

The `bug.js` file shows the erroneous code. The `bugSolution.js` file provides the corrected version.

## Problem

Directly modifying the `count` variable inside the `useEffect` hook doesn't trigger a re-render.  React's state management relies on calling the `setCount` function to update the state and initiate a re-render.  This error can be difficult to spot, especially in more complex components.