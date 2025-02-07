# Node.js Server Hanging on Long Requests

This repository demonstrates a common issue in Node.js where a server hangs due to a long-running synchronous operation blocking the event loop.  The `server.js` file shows the problematic code, while `serverSolution.js` provides a solution using asynchronous operations.

## Problem

The original code performs a 5-second synchronous `while` loop inside the request handler. This blocks the event loop, preventing the server from handling other requests and leading to unresponsiveness.

## Solution

The solution uses asynchronous operations (e.g., `setTimeout`) to simulate the long-running task without blocking the event loop.  This ensures the server remains responsive, even during lengthy operations.