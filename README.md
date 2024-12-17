# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug: an infinite loop caused by a missing dependency in the `useEffect` hook. The `useEffect` hook is used to perform side effects after render. If you don't list all the variables used inside the effect function in the dependency array, it may cause infinite re-renders.

## Bug Description

The `bug.js` file contains a component with a `useEffect` hook that is missing a crucial dependency.  This results in an infinite render loop, causing performance issues and potentially crashing the application.

## Solution

The `bugSolution.js` file provides the corrected code. The solution adds the `count` variable to the `useEffect` hook's dependency array, fixing the infinite loop.  By including `count` as a dependency, the effect only runs when the value of `count` changes.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install the necessary dependencies.
3. Run `npm start` to start the development server.
4. Observe the console output for the infinite loop in the original bug. Then compare the corrected version.