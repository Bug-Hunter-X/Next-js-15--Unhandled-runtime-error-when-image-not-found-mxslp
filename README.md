# Next.js 15 Unhandled Image Error

This repository demonstrates an uncommon error in Next.js 15 where a runtime error caused by an unfound image is not properly handled, leading to a blank page instead of a user-friendly error message.  This differs from other Next.js errors that are caught and displayed gracefully. 

## Bug Description
The `pages/about.js` file attempts to load an image that does not exist.  Next.js 15 does not automatically catch or display this error to the user; instead, the page renders blank.

## Solution
The issue is resolved in `pages/aboutSolution.js` by wrapping the image import and display within a try-catch block.  This allows for handling the `Error` thrown by `require()` when the image is not found.  Additionally, this example includes a fallback image in case the image fails to load.