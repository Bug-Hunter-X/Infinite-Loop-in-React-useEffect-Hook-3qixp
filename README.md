# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: creating an infinite loop by incorrectly specifying the dependency array.

## The Bug

The `bug.js` file contains a component that uses `useEffect` to log the current count.  However, the dependency array is missing, causing the effect to run after every render, leading to an infinite loop.  The component re-renders continuously because the `count` variable changes inside the `useEffect` hook, triggering another render, and so on. 

## The Solution

The `bugSolution.js` file shows the corrected code. The dependency array `[count]` is correctly included, ensuring the effect only runs when the value of `count` changes. This prevents the infinite loop.

## How to reproduce

1. Clone this repository
2. Navigate to the `bug` directory and run `npm install`
3. Run `npm start` to see the buggy component.
4. Navigate to the `bugSolution` directory and run `npm install`
5. Run `npm start` to see the fixed component.