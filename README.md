# React useEffect Runs on Every Render Despite Empty Dependency Array

This repository demonstrates a subtle bug in React where a `useEffect` hook with an empty dependency array still runs on every render. This is often unexpected and can lead to performance issues.  The root cause is related to how component updates and the timing of effect execution are handled.  The solution involves carefully considering the effect's dependencies and optimizing to prevent unnecessary executions.

## Bug
The bug lies within the `MyComponent` function. Even though the dependency array is empty, `useEffect` runs on every render, logging 'Effect ran!' to the console. 

## Solution
The solution involves restructuring the component or effect to ensure that the effect's dependencies are correctly declared.