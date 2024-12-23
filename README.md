# Unhandled Exception in Node.js HTTP Server

This repository demonstrates a common error in Node.js applications: unhandled exceptions within HTTP request handlers.  Unhandled exceptions can cause your server to crash unexpectedly, leading to downtime and data loss.  This example showcases the problem and provides a solution.

## The Bug

The `bug.js` file contains an HTTP server that throws an exception when the URL is `/error`.  Because this exception isn't caught within the request handler, it propagates up and crashes the server.

## The Solution

The `bugSolution.js` file demonstrates how to properly handle exceptions within the request handler, preventing the server from crashing.  A `try...catch` block is used to gracefully handle errors and send appropriate responses to the client.

## How to Run

1. Clone this repository.
2. Navigate to the repository directory.
3. Run `node bug.js` to see the server crash when accessing `/error`.
4. Run `node bugSolution.js` to see the improved error handling.