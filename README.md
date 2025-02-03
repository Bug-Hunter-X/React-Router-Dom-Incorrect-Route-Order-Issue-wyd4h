## React Router Dom Route Order Issue

This repository demonstrates a common issue encountered when using React Router Dom's `Routes` component.  The problem arises from the order in which routes are defined, specifically when using a catch-all route (`*`).

### Problem
The `App.js` file contains an incorrect route order, causing the catch-all route to take precedence, and other routes to not work correctly. This leads to the `NotFound` component being displayed even when navigating to `/` or `/about`.

### Solution
The solution involves reordering the routes within the `Routes` component. The catch-all route (`*`) should always be the last route defined to ensure it only matches URLs not covered by more specific routes.

### How to reproduce
1. Clone the repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe that navigating to `/` or `/about` will always show the `404 Not Found` page.

### How to fix
1. Modify the `App.js` file according to the corrected code in `App.js`.
2. Rerun `npm start`.
3. Observe that navigating to `/` or `/about` now shows the correct components.