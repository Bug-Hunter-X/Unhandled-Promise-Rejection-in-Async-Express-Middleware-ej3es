# Unhandled Promise Rejection in Async Express Middleware

This repository demonstrates a common error in Express.js applications where errors thrown within asynchronous middleware functions are not properly handled, leading to unhandled promise rejections and potential server crashes.  The bug and its solution are outlined below.

## Bug

The `bug.js` file contains an Express.js app with a route that fetches user data asynchronously. If an error occurs during the data fetching (e.g., database connection error), the error is not caught by the error handling middleware, resulting in an unhandled promise rejection.

## Solution

The `bugSolution.js` file demonstrates the correct way to handle asynchronous errors. It utilizes `async/await` and a `try...catch` block within the route handler to capture and handle any potential errors gracefully.