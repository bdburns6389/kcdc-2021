# The Tao of Refactoring

- Working effectively with legacy code - Book to read

## Why Refactor

- Code clean
- Improve performance
  -Save time mone
  -Make bugs easier to be found
  -Improves the system desing

## When to refactor

- You don't decide to refactor, you refactor because you want to do something else, and refactoring helps you do that other thing -- Martin Fowler

## When to not refactor

- When the code is unusable and you need a rewrite.
- When you are close to a deadline.

## Quickest places to start refactoring

- Refactor when you add a function
- Refactor when you need to fix a bug
- Refactor as you do a code review

## The rule of three _Don Roberts_

- First time you do something just do it
- The second time you do it, take note but do it the duplicate way anyway.
- The third time you do something, refactor.

### Changing the code without changing the behavior?

- Pick one side and go for it, you will start to notice patterns
- To refactor we should have tests. To put test in place we must refactor.

### Type of code smells

- Singletons
- Internal instantiaion
- Use of external resources

### Seams

- A place where you can alter behavior in your program without editing it in that place.

## Gilded rose kata?

- Kata to help you learn how to better refactor code.
