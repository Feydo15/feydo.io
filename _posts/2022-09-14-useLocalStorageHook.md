---
Layout:
Title: "useLocalStorage Hook "
Date: 2022-09-14
Categories:
---

# Introduction
today i have learned about useLocalStorage Hook
well Hooks are a feature in React that allow you use state and other React features without writing classes.
# body

useLocalStorage hook
Sync state to local storage so that it persists through a page refresh. Usage is similar to useState except we pass in a local storage key so that we can default to that value on page load instead of the specified initial value.

Since the local storage API isn't available in server-rendering environments, we check that typeof window !== "undefined" to make SSR and SSG work properly.

i have used it in my app so that I can use my previous state even if i reload the page.

# conclusion
useLocalStorage hook is  Similar to useState but first arg is key to the value in local storage.