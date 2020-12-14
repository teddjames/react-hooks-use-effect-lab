# React useEffect Lab

## Overview

In the labs for this section, we're going to be building a trivia app! The first
feature we're going to work on is the Question component.

There is some starter code for us to work with. There's a Question component
already set up to display the question and a list of possible answers. It's also
hooked up to its parent component, App, so that it has access to all the props
it needs.

The feature we're going to build out using `useEffect` is a **countdown timer**,
so that the user has to answer each question within 10 seconds.

## Deliverables

When the Question component renders, create a side effect using `useEffect` and
use `setInterval` to run a callback function every 1 second.

Inside the callback function, use the `setTimeRemaining` function to decrease
the amount of time remaining by 1 every 1 second.

When the `timeRemaining` hits 0, do the following:

- reset `timeRemaining` back to 10 seconds, so our next question will have a
  fresh timer; and
- call the `onAnswered` callback prop with a value of false
  (`onAnswered(false)`), to trigger some behavior in the App component.

You should _also_ use the **cleanup function** for `useEffect` to clear the
interval between renders.

Make sure to pay attention to any warning/error messages in the console as a
result of using `useEffect`, and clean them up by providing any necessary
_dependencies_ in the second argument of `useEffect`.

If you're stuck on getting the interval working, or encountering some strange
behavior, make sure to check out the resources below!

## Resources

- [setInterval in Using Hooks](https://upmostly.com/tutorials/setinterval-in-react-components-using-hooks)
- [React Docs on useEffect][useeffect-hook]
- [A Complete Guide to useEffect](https://overreacted.io/a-complete-guide-to-useeffect/)

[side-effects]: https://en.wikipedia.org/wiki/Side_effect_(computer_science)#:~:text=In%20computer%20science%2C%20an%20operation,the%20invoker%20of%20the%20operation.
[useeffect-hook]: https://reactjs.org/docs/hooks-effect.html
