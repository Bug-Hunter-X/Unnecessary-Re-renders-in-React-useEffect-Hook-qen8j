# Unnecessary Re-renders in React useEffect Hook

This repository demonstrates a common React bug involving unnecessary re-renders within a `useEffect` hook.  The `useEffect` hook, without a dependency array, runs after every render, leading to performance degradation, especially in complex components.

## The Bug
The `bug.js` file contains a component where the `useEffect` hook logs a message to the console after every render. This is inefficient, as the console log is not dependent on any state changes. 

## The Solution
The `bugSolution.js` file provides a corrected version. By adding `[count]` as a dependency array, the `useEffect` now only runs when the `count` state variable changes, optimizing performance.