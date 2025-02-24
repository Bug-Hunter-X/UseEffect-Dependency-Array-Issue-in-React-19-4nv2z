# React 19 useEffect Dependency Array Issue

This repository demonstrates a common error related to the `useEffect` hook in React 19 and how to fix it.

## Problem

The provided `MyComponent` uses `useEffect` without including `count` in the dependency array. This causes the effect to run after every render, leading to unnecessary re-renders and potential performance issues.

## Solution

To resolve this, include `count` in the dependency array. Now the effect will run only when the value of `count` changes.

## How to reproduce

1. Clone this repo
2. Run `npm install`
3. Run `npm start`
4. Observe the console logs. You'll see that the effect is run after each render in the buggy version but only when the count changes in the fixed version.