# React Infinite Render Loop Bug
This repository demonstrates a common React bug: an infinite render loop caused by an improperly used `useEffect` hook.  The `useEffect` hook, while powerful, can easily lead to unexpected behavior if not used correctly.

## Problem
The `MyComponent` function uses `useEffect` without specifying dependencies.  This means the effect runs after every render, causing an infinite loop because the log statement causes re-renders. 

## Solution
The solution involves adding an empty dependency array `[]` to the `useEffect` hook. This ensures that the effect only runs once after the initial render.