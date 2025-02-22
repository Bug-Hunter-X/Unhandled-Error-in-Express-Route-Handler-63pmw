# Express.js Route Handler Error

This repository demonstrates a common error in Express.js route handlers: lack of error handling for invalid input.  The `bug.js` file shows the erroneous code, and `bugSolution.js` provides the corrected version.

The bug occurs when the route handler `/users/:id` attempts to parse the `id` parameter as an integer without validating the input. If a non-numeric `id` is provided, `parseInt()` will return `NaN`, leading to potential unexpected behavior or crashes.

The solution adds error handling to check if the `id` is a valid integer before proceeding.  It returns a 404 error if the user is not found.