# React useEffect Hook Missing Cleanup Function

This repository demonstrates a common error in React's `useEffect` hook: omitting the cleanup function.  The example shows how forgetting to return a cleanup function can lead to memory leaks and unexpected behavior.

## Bug

The `bug.js` file contains a `MyComponent` that uses `useEffect` without a cleanup function. This means that even after the component unmounts, the effect's logic continues to run. In this specific example, a log message is printed to the console, but in a real-world scenario, this could involve network requests, timers, or subscriptions that persist unnecessarily. This can result in memory leaks and unexpected side-effects.

## Solution

The `bugSolution.js` file corrects this issue by providing a cleanup function that ensures proper resource release when the component unmounts. This prevents memory leaks and improves application stability.

## How to Run

1. Clone this repository.
2. Navigate to the directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.

The React application will demonstrate the difference between the buggy and corrected versions of the component.