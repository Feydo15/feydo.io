---
Layout:
Title: "React useContext Hook"
Date: 2022-09-15
Categories:
---

# Introduction
today i have learned about React useContext Hook
React Context is a way to manage state globally.
well Hooks are a feature in React that allow us to use state and other React features without writing classes.
# body

It can be used together with the useState Hook to share state between deeply nested components more easily than with useState alone.

but the problem is that State should be held by the highest parent component in the stack that requires access to the state.

To illustrate, we have many nested components. The component at the top and bottom of the stack need access to the state.

To do this without Context, we will need to pass the state as "props" through each nested component. This is called "prop drilling".

for example, <import { useState } from "react";
import ReactDOM from "react-dom/client";

function Component1() {
  const [user, setUser] = useState("Jesse Hall");

  return (
    <>
      <h1>{`Hello ${user}!`}</h1>
      <Component2 user={user} />
    </>
  );
}

function Component2({ user }) {
  return (
    <>
      <h1>Component 2</h1>
      <Component3 user={user} />
    </>
  );
}

function Component3({ user }) {
  return (
    <>
      <h1>Component 3</h1>
      <Component4 user={user} />
    </>
  );
}
>

well i have used this useContext hook to create my application context that covers the entire application
now i can pass my props fast and easy along my app.

# conclusion
useContext hook works hand in hand with Create Context o create context, you must Import createContext and initialize it: and Context Provider which Wrap child components in the Context Provider and supply the state value.