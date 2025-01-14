# Express.js Asynchronous Operation Bug
This repository demonstrates a common issue in Express.js applications where slow response times result from improper handling of asynchronous operations within request handlers.

## Bug Description
The `bug.js` file contains an Express.js server with a route handler that simulates an asynchronous operation using `setTimeout`. This introduces a 5-second delay before sending the response. In real-world scenarios, this could be a database query, external API call, or any other time-consuming task.

This delay can lead to slow response times and poor user experience.  If multiple requests are handled concurrently, the server's responsiveness can degrade substantially. 

## Solution
The `bugSolution.js` file demonstrates how to address the issue by properly handling asynchronous operations using Promises or async/await. This ensures that the server does not block while waiting for the asynchronous operation to complete.