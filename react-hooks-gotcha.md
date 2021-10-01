# React Hooks Gotchas

- Virtual DOM rendering is faster, but Virtual DOM diffs are expensive.
- Avoid Virtual DOM diffs.
- Function component IS just the render function
- this means a class component can re run render without the rest of the code, but a functional component EVERYTHING re-runs.

## Hooks

- React hooks are not about state, but memoization.
- All hooks memoize values

### Memorandum - to be rememebered

useState always forces a rerender.

## Hooks are tedious

- Eslint doesn't catch custom hooks
- Lack of knowledge can hurt you
- Hooks NEED memoization.
- Class component already had memo.
- Redux connect() memoizes components

## Default prop values

- defaultProps is deprecated
- Create function outside of component function, then refer to it inside the component.
- Can also use Function.prototype as a default prop as a no-op function call as a prop.

### Clear all functions in useEffect using a retun statement.

-- E.G. setTimeouts should be cleared in use effect to prevent memory leak.

# Memoize all the Things!!!

## Kevin Ghadyani youtube channel

## Kevin Ghadyani - Extended cut youtube channel

https://docs.oneform.dev
https://github.com/sawtaytoes
