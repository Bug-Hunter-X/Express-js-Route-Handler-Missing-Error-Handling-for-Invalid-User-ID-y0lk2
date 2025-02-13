# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of error handling when parsing user input.  Specifically, the code attempts to parse a user ID as an integer without verifying that the input is numeric. This can lead to unexpected behavior or crashes.

## Bug

The `bug.js` file contains an Express.js route that fetches a user by ID.  It attempts to parse the ID from the request parameters as an integer and uses it to find the user.  However, it fails to handle the case where the ID is not a number, leading to an error if a non-numeric ID is provided.

## Solution

The `bugSolution.js` file demonstrates the corrected code.  It adds error handling to check if the ID is a number before attempting to parse it. If the ID is not a number, a 400 Bad Request error is returned.