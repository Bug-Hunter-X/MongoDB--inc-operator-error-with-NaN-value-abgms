# MongoDB $inc Operator Error

This repository demonstrates a common error when using the `$inc` operator in MongoDB: attempting to increment a field with a non-numeric value such as NaN. The `bug.js` file shows the erroneous code, while `bugSolution.js` provides the corrected version.

## How to Reproduce

1. Clone this repository.
2. Make sure you have MongoDB and a Node.js driver installed.
3. Create a MongoDB collection called `myCollection`. Add a document with an integer field named `count`.
4. Run `bug.js`. This will throw a MongoDB error.
5. Run `bugSolution.js` to see the correct implementation.

## Solution
The solution involves type checking and handling non-numeric values appropriately before updating the document.   Always ensure that the value you're passing to `$inc` is a valid number.