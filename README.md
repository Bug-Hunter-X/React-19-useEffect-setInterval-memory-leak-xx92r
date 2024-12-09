# React 19 useEffect setInterval memory leak
This example demonstrates a common mistake when using setInterval within a React useEffect hook.  Forgetting to include a cleanup function leads to memory leaks. The bug.js file shows the erroneous code. The bugSolution.js file provides a corrected version.

## Bug
The bug lies in the improper use of `setInterval` within the `useEffect` hook. Without a cleanup function, the interval continues indefinitely, even after the component unmounts, causing a memory leak. 

## Solution
The solution involves adding a return function to the `useEffect` hook.  This function clears the interval when the component unmounts or when the dependency array changes, preventing the memory leak.
