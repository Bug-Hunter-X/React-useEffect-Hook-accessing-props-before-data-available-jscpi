# React useEffect Hook accessing props before data available

This repository demonstrates a common error in React applications where the `useEffect` hook attempts to access props before the data has been fetched asynchronously, leading to unexpected behavior or errors.

The `bug.js` file showcases the problematic code.  The `bugSolution.js` provides a corrected version.

## Problem
The issue arises because the `useEffect` hook, despite using an empty dependency array `[]`, attempts to access `props.data` before the data is populated.  If `props.data` is fetched asynchronously, there is a chance that `useEffect` will run before the data is available, resulting in an error or unexpected rendering.

## Solution
The solution involves adding a check to ensure that `props.data` is available before trying to use it.  The solution also showcases how to handle the loading state effectively.