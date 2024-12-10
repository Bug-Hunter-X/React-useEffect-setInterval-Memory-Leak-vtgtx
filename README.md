# React useEffect setInterval Memory Leak

This repository demonstrates a common bug in React applications: memory leaks caused by improper usage of `setInterval` within the `useEffect` hook.  The `setInterval` function, without proper cleanup, continues running even after the component unmounts, leading to memory leaks and potential performance issues.  The solution demonstrates how to correctly use `setInterval` to avoid this problem.

## Bug

The `bug.js` file contains a React component that uses `setInterval` to update a counter every second. However, it lacks a cleanup function to stop the interval when the component unmounts.