# Express.js Route Handler Error

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.

The `bug.js` file shows the problematic code.  The `bugSolution.js` file provides a corrected version with proper error handling.  The issue is that the code attempts to convert the user ID to an integer using `parseInt` without checking if the result is a valid number.  If the `userId` is not a valid integer (e.g., it's a string or contains non-numeric characters), this will cause unexpected behavior, potentially leading to crashes or incorrect responses.

The solution includes a check to ensure the `userId` is a number before proceeding.  If it's not a number, it sends a 400 Bad Request response to the client.