# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js where a long-running task in the request handler blocks the event loop, causing the server to become unresponsive. The `server.js` file contains the buggy code, and `server-solution.js` provides a solution using asynchronous operations.

## Problem

The original `server.js` uses a simple `for` loop to simulate a long-running task.  This loop occupies the event loop, meaning no other requests can be processed until it completes.  This causes the server to hang and become unresponsive.

## Solution

The `server-solution.js` file demonstrates how to fix this by using asynchronous operations to perform long-running tasks.  This allows other requests to be processed while the long-running task runs in the background.