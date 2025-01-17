# React 19 useEffect Cleanup Function Memory Leak

This repository demonstrates a common error in React 19 related to the `useEffect` hook and its cleanup function.  Improperly handling cleanup in `useEffect` can lead to memory leaks, especially when dealing with asynchronous operations or subscriptions.

## Problem

The provided code snippet shows a `MyComponent` that increments a counter.  The `useEffect` hook is used with an empty dependency array `[]`, indicating it should run only once after the component mounts.  However, the cleanup function is incomplete.  This missing cleanup logic can lead to memory leaks if the component unmounts before the cleanup process is done.