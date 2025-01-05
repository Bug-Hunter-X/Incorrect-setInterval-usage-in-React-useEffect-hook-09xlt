# Incorrect setInterval usage in React useEffect hook
This repository demonstrates a common mistake when using setInterval within a React useEffect hook. The issue arises from incorrectly providing a direct state update call to setInterval instead of a function expression.

## Bug Description:
The provided code attempts to increment a counter every second. However, because setCount(count + 1) is executed immediately instead of being wrapped in a function, the interval will update the counter only once.

## Solution:
The correct implementation involves wrapping the state update logic in a function expression. This ensures the count is updated at each interval call.

## How to reproduce the bug:
1. Clone the repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the counter's behavior.  It won't increment correctly.

## How to fix the bug:
Refer to the bugSolution.js file for the corrected code.  It properly increments the count each second.