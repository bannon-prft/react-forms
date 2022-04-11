# React Forms and User Input

Building Forms and User Input in React from [React - The Complete Guide (incl Hooks, React Router, Redux)](https://www.udemy.com/course/react-the-complete-guide-incl-redux/)

## Key Concepts

- When to validate:
	- when form is submitted - avoid unnecessary warnings but maybe present feedback too late
	- when input is losing focus - useful for untouched forms, but may be not ideal if fixing errors in a specific input
  - on every keystroke - if applied only on invalid inputs, has the potential to provide more direct feedback
- event.preventDefault()
  - use this on form submission if the form is submitted with a button because if the form is submitted with a button, the default browser behavior is to send an HTTP request to the server
  - in this app, there is no server to send the request to
  - would restart the entire application, and would lose the state
- useRef or useState for input values
  - if only interested in it once, when form is submitted, useRef is better
  - if entered value is needed after every keystroke, useState is better
- use a custom hook to manage all the state logic for forms with multiple inputs that share much logic
  - use aliases when pulling in the same keys for multiple inputs
- useReducer() added because we have related pieces of state managing independent pieces of state
  - not necessary here but used for practice
  - useReducer takes a `reducer function` and `initial state` as arguments
    - returns `[state, dispatchFunction]`
    - reducer function takes `prevState`, `action` as arguments
      - returns some form of state, with a default set
  
