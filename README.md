# React useEffect Infinite Loop Bug
This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing or incorrect dependency array.  The `useEffect` hook, while powerful, can lead to unexpected behavior if not used carefully.

## Bug Description
The `bug.js` file contains a component that uses `useEffect` to log the current count. However, because it's missing the correct dependency, it re-renders infinitely, causing performance issues.

## Solution
The `bugSolution.js` file provides the corrected code. By including `[count]` in the dependency array, the effect only runs when the `count` value changes, resolving the infinite loop.

## How to Reproduce
1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the infinite loop in the console and the excessively high CPU usage.
5. Replace `bug.js` with `bugSolution.js` to see the corrected behavior.