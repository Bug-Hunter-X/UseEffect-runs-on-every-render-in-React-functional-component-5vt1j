# Uncommon React useEffect Bug

This repository demonstrates a subtle bug related to the `useEffect` hook in React functional components.  The `useEffect` hook is intended to perform side effects, but in this case, it runs more frequently than expected.

## Bug Description

The `useEffect` hook, even with a dependency array `[count]`, triggers on every render.  This is unexpected behavior and can lead to performance issues and unexpected side effects.

## Solution

The issue was caused by the fact that the value of 'count' is updated in the useEffect which means the count will be updated infinitely. To solve the issue, a new value should be set instead of updating the existing one.