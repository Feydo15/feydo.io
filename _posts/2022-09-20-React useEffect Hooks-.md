---
Layout:
Title: "React useEffect Hooks"
Date: 2022-09-20
Categories:
---

# Introduction
today i have learned about React useEffect Hooks
The useEffect Hook allows you to perform side effects in your components.
Some examples of side effects are: fetching data, directly updating the DOM, and timers.
well Hooks are a feature in React that allow us to use state and other React features without writing classes.
# body

useEffect accepts two arguments. The second argument is optional.

useEffect(<function>, <dependency>)
Use setTimeout() to count 1 second after initial render: It keeps counting even though it should only count once!

useEffect runs on every render. That means that when the count changes, a render happens, which then triggers another effect.

This is not what we want. There are several ways to control when side effects run.

We should always include the second parameter which accepts an array. We can optionally pass dependencies to useEffect in this array.
So, to fix this issue, let's only run this effect on the initial render.

Here is an example of a useEffect Hook that is dependent on a variable. If the count variable updates, the effect will run again: <import { useState, useEffect } from "react";
import ReactDOM from "react-dom/client";

function Counter() {
  const [count, setCount] = useState(0);
  const [calculation, setCalculation] = useState(0);

  useEffect(() => {
    setCalculation(() => count * 2);
  }, [count]); // <- add the count variable here

  return (
    <>
      <p>Count: {count}</p>
      <button onClick={() => setCount((c) => c + 1)}>+</button>
      <p>Calculation: {calculation}</p>
    </>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Counter />);

>


# conclusion 

if there are multiple dependencies, they should be included in the useEffect dependency array.
