# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The provided code creates an infinite loop by logging the count within the effect without specifying dependencies.  This leads to unnecessary re-renders and performance degradation.  The solution demonstrates how to properly utilize dependencies in useEffect to resolve this issue.

## Bug Description

The `useEffect` hook in the provided code lacks dependencies, causing it to execute after every render.  The `setCount` function is called, updating the count, which triggers another render and another execution of the effect. This creates an infinite loop, resulting in significant performance issues.

## Solution

The solution adds a dependency array `[count]` to the `useEffect` hook.  This ensures that the effect only runs when the `count` value changes, preventing the infinite loop.