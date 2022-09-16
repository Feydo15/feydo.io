---
Layout:
Title: "React useReducer Hook"
Date: 2022-09-15
Categories:
---

# Introduction
today i have learned about React useReducer Hook
The useReducer Hook is similar to the useState Hook. It allows for custom state logic.
well Hooks are a feature in React that allow us to use state and other React features without writing classes.
# body

The useReducer Hook accepts two arguments. useReducer(<reducer>, <initialState>) The reducer function contains your custom state logic and the initialState can be a simple value but generally will contain an object. The useReducer Hook returns the current state and a dispatch method.

useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one. useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.

# conclusion
If you find yourself keeping track of multiple pieces of state that rely on complex logic, useReducer may be useful.
