# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook. The bug arises from an incomplete dependency array, leading to an infinite loop.

## Bug Description

The `MyComponent` function uses the `useEffect` hook to log the current value of the `count` state variable. However, the initial implementation lacks `count` in the dependency array. This causes the effect to run after every render, creating an infinite loop of updates and rendering.

## Solution

The solution involves adding `count` to the dependency array of the `useEffect` hook. This ensures the effect only runs when the `count` variable changes.