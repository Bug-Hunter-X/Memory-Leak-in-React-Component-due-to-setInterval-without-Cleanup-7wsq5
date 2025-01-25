# React setInterval Cleanup Bug
This repository demonstrates a common bug in React applications: using `setInterval` within a `useEffect` hook without proper cleanup. This can lead to memory leaks and unexpected behavior.

## The Problem
The provided `MyComponent` uses `setInterval` to update the count every second.  However, it fails to clear the interval when the component unmounts. This means that even after the component is removed from the DOM, the interval continues to run, consuming resources and potentially interfering with other parts of the application.

## The Solution
The solution involves using the return value of `useEffect` to clear the interval when the component unmounts.  This ensures that the interval is stopped when it's no longer needed.

## How to run
1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.