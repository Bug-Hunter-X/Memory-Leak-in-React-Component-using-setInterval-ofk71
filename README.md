# React setInterval Memory Leak
This repository demonstrates a common bug in React applications involving the `setInterval` function within the `useEffect` hook, leading to memory leaks.  The `bug.js` file showcases the incorrect implementation, while `bugSolution.js` provides the corrected version.

**Problem:**
The provided code uses `setInterval` without a cleanup function. This means that even when the component unmounts, the interval continues to run, leading to a memory leak. 

**Solution:**
The corrected code uses the return value of `useEffect` to implement a cleanup function that clears the interval before the component is unmounted. This prevents the memory leak. 