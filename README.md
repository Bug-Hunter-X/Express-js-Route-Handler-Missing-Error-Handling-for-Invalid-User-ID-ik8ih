# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  missing error handling for invalid input.  Specifically, this example shows a route that fetches a user by ID.  The code fails to handle the case where the user ID is not a valid integer, leading to potential crashes or unexpected behavior.

## Bug

The `bug.js` file contains the flawed code. It attempts to parse the user ID as an integer without checking for errors. If the ID is not a valid integer, `parseInt(userId)` will return `NaN`, leading to issues when comparing it to user IDs in the database.

## Solution

The `bugSolution.js` file provides a corrected version. It includes explicit error handling to check if the ID is a valid integer and gracefully handles the case where the user is not found or the ID is invalid.