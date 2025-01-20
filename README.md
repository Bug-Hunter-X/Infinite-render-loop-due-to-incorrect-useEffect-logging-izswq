# React useEffect Infinite Render Loop Bug
This repository demonstrates a common React bug: an infinite render loop caused by incorrectly logging state variables within the `useEffect` hook. 

## Bug Description
The `MyComponent` component uses `useState` to manage a count. The `useEffect` hook intends to log the count to the console. However, because it's missing the dependency array, it runs on every render. Logging from within the hook triggers another render, creating an infinite loop. 

## Solution
The solution involves properly specifying the dependencies for the `useEffect` hook. Adding `count` in the dependency array ensures it runs only when the `count` value changes. 

## How to reproduce the bug:
1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Open your browser and observe the infinite logging and potential browser crash.

## How to fix the bug
1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Check `bugSolution.js` file for the corrected code. 
4. Run `npm start` to start the development server.
5. Observe that the logging occurs correctly without causing an infinite loop.