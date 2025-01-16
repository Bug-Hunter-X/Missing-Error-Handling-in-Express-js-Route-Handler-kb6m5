# Express.js Route Handler Error Handling Bug

This repository demonstrates a common error in Express.js route handlers:  missing error handling for invalid input.  The `bug.js` file contains the buggy code, while `bugSolution.js` provides the corrected version.

**Bug:** The route handler for `/users/:id` attempts to parse the `id` parameter as an integer without checking for errors. If a non-numeric ID is passed, this will cause unexpected behavior (e.g., a crash) rather than returning a proper error response.

**Solution:** The corrected code includes error handling using a `try...catch` block to gracefully handle the case where the ID is not a valid number and returns an appropriate HTTP status code (400 Bad Request) with an error message.