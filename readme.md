#Explanation of using async/Await instead of callbacks->
This code uses Promises (via fs/promises) and try/catch blocks instead of the older callback style for a few practical reasons. First off, it just makes the code easier to read and follow. With callbacks, you end up nesting functions inside functions, and before you know it, you’ve got this tangled "pyramid" of code that’s hard to debug. Promises let us write the same logic in a more straightforward, step-by-step way using async/await, almost like it’s synchronous code
Error handling also becomes much cleaner. Instead of checking for errors in every single callback (which gets repetitive fast), we can wrap all our file operations in one try/catch block. If anything goes wrong—like the file doesn’t exist, or we don’t have permission—the error gets caught in one place, and we can send a consistent response to the client. With callbacks, you’d have to handle errors separately for each filesystem operation, which is more work and easier to mess up.
Plus, Promises are just the modern way to handle async code in JavaScript. Callbacks aren’t going away, but Promises (and async/await) are the recommended approach for new code because they’re more flexible and easier to work with once you get the hang of them. So in short: simpler code, better errors, and staying up-to-date with how Node.js is meant to be written these days.
#Main reasons to use async/await->
Improves readability by writing asynchronous code in a synchronous-like manner.
Avoids callback hell by eliminating deeply nested function calls.
Centralized error handling using try...catch instead of checking err repeatedly.
Easier to debug due to clearer and more linear stack traces.
Better code maintainability as logic is cleaner and easier to update or extend.