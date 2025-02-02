# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js applications: server unresponsiveness caused by a long-running synchronous operation that blocks the event loop.  The `server.js` file contains a problematic server implementation.  The `serverSolution.js` file provides a corrected version using asynchronous operations.

## Problem

The server in `server.js` performs a long-running computation (simulated by a `while` loop) synchronously within the request handler. This blocks the event loop, preventing Node.js from handling other requests while the loop is running.  This leads to the server becoming unresponsive to new connections.

## Solution

The solution, found in `serverSolution.js`, employs asynchronous operations or offloads long-running tasks to avoid blocking the event loop. This ensures the server remains responsive even during lengthy operations.