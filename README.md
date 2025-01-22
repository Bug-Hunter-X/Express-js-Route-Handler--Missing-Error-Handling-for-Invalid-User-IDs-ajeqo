# Express.js Route Handler: Missing Error Handling for Invalid User IDs

This repository demonstrates a common error in Express.js route handlers: the lack of error handling for invalid input. Specifically, this example shows a route that fetches a user by ID. If the ID is not a number, the application may crash or return unexpected results.

## Bug
The `bug.js` file contains the erroneous code.  The route handler attempts to parse the user ID as an integer without checking for potential errors.  If a non-numeric ID is provided, `parseInt(userId)` will return `NaN`, leading to issues in the `find()` method.

## Solution
The `bugSolution.js` file provides a corrected version. It includes error handling to check if `userId` is a valid number before attempting to parse it and find the corresponding user.  If the ID is invalid, an appropriate error response (400 Bad Request) is returned.