# Unhandled 'error' event in Node.js HTTP server

This repository demonstrates a common error in Node.js where an unhandled 'error' event causes the server to crash without providing sufficient debugging information.

## Bug

The `bug.js` file contains a simple HTTP server.  However, it lacks proper error handling.  If any error occurs during request processing (e.g., JSON.stringify failure due to malformed data, network issues, etc), the server crashes silently. This makes identifying and resolving issues extremely challenging.

## Solution

The `bugSolution.js` file provides a corrected version of the server. It includes comprehensive error handling using `try...catch` blocks to gracefully handle potential exceptions and log detailed error messages.  This aids in the efficient detection and correction of unexpected errors. 