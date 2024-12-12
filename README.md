# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in a request handler can cause the server to become unresponsive.  The `bug.js` file contains the problematic code, while `bugSolution.js` provides a solution using asynchronous operations.

## Problem

The server in `bug.js` simulates a long-running task that occupies the event loop for five seconds. During this time, the server is unable to handle new requests, resulting in unresponsive behavior.

## Solution

`bugSolution.js` demonstrates how to resolve this by using asynchronous operations such as `setTimeout` or promises. This allows the event loop to remain responsive and handle new requests while the long-running task is executing in the background.  Asynchronous operations are key to maintaining responsiveness in Node.js.