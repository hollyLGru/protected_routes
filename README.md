## Setup

Clone this repo and run `npm i` and then `npm start`

## Project Instructions


- In the `Router.js` file we can see a list of all our routes and paths. Write a `ProtectedRoute` function under the appropriate comment.

- Write a `checkAuth` function under the appropriate comment. Use the `cookie` module to parse the browser cookies and check the `loggedIn` cookie. If it has a value, return `true` otherwise return `false`.

- Replace all the element properties in our `Route` components (inside of `Routes`) with `<ProtectedRoute />` EXCEPT for the "/login" route. We always want to be able to access that so leave it alone.

  - Dont forget to also add the component property to the `<ProtectedRoute />` element in which the Route should render. For example, if the route is "/about", we would want to pass our "About" component in the component property:
  - `<ProtectedRoute component={ About }/>`

- Upon making the changes to these `Route`'s you should notice that you can no longer access any of the links in the navigation bar. They send you back to the login page because there is no cookie available. Let's make sure we set one when we log in.

- Go to the `Login` component (under `src/components/Login.js`) and look at the login function. There is a comment to a the cookie. Set a cookie equal to the following value: `loggedIn=true;max-age=60*1000`.

- Notice you can now login and access the pages appropriately. We've set an expiration time of one minute on the cookie so go do something else for a minute and then come back to this site. Refresh the page. Were you directed back to the login page?

- Also, the "logout" button will also delete the cookie and navigate you back to the '/login' screen.
