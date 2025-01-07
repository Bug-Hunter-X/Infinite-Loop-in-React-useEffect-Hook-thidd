# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug causes an infinite loop due to a missing dependency in the `useEffect` call.

## Bug Description
The `useEffect` hook is designed to perform side effects after a component renders.  However, if a value used within the effect isn't included in the dependency array, the effect will run on every render, creating an infinite loop.

## How to Reproduce
Clone this repository and run `npm install` to install dependencies. Then, run `npm start` to start the development server.
You'll observe the console logging 'Count updated' continuously, indicating the infinite loop. 

## Solution
The solution involves ensuring that all values accessed within the `useEffect` are included in the dependency array. 