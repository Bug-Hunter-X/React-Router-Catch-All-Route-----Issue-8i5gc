# React Router Catch-All Route Issue

This repository demonstrates a common issue encountered when using the catch-all route (`*`) in React Router v6.  The problem occurs when the catch-all route is placed after other routes. This leads to the catch-all route being ignored despite it being intended to handle all non-matching routes. The example below has a `Home`, `About` and a `NotFound` component that is intended to be the catch all component that is never displayed. 

## Solution

The solution involves carefully ordering the routes.  The catch-all route (`*`) must always be placed last in the `Routes` component. This ensures that it only catches routes that haven't been matched by other, more specific routes.  See `AppSolution.js` for the corrected code.