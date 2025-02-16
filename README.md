# Unhandled Promise Rejection in Express.js

This repository demonstrates a common error in Express.js applications: failing to handle promise rejections in asynchronous operations.  Without proper error handling, these rejections can lead to silent failures and make debugging difficult.

The `bug.js` file showcases the problematic code. The `someAsyncOperation` function simulates an asynchronous operation that can either succeed or fail.  However, the error handling in the Express route is incomplete; it only logs the error to the console but doesn't send an appropriate response to the client or otherwise manage the error.

The solution, provided in `bugSolution.js`, demonstrates the correct way to handle promise rejections.  A central error handler is implemented to catch unhandled rejections and send a user-friendly error response to the client, improving application resilience and making error analysis easier.
