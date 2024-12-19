# React useEffect Cleanup Issue

This repository demonstrates a common issue with React's `useEffect` hook: improper handling of the cleanup function when a component unmounts.  The provided `MyComponent` demonstrates a scenario where the cleanup function (`return () => { ... }`) does not correctly handle the component's unmount, which might lead to unexpected side effects or memory leaks in more complex applications.

The solution provided shows how to correctly handle the cleanup procedure in such situations, which is crucial for maintaining a clean and predictable application.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs and how the component behaves upon mounting and unmounting.  The problematic implementation is in `bug.js` and corrected in `bugSolution.js`.

## Solution

The solution involves carefully managing the cleanup within the useEffect function's return.  Ensuring that any long-running tasks, subscriptions, or timers are properly cleaned up when the component unmounts is paramount to prevent these issues.
