# React

## State
- keep track of values that could change through interactions or fetching data
- application state: data pull from backend
- view state: 
## Props
- arguments passed to function
- should not be modified

## Effect ~ Hooks
- something that happens aside from returning JSX
- codifies and encapsulate side effects

### useEffect
- no array, run everytime
- empty array, run once
- array of variables, run when either variables change

## Custom Hooks
- hooks folder
- always starts with the word 'use'<blah>

## useCallback
- memoize (???)

## useRef

## Resources
- useHooks.com

## Immutable Data Patterns
- easier way to track changes
- making copies for comparison
- guarantee thread safety - accessing the same thing at the same time

- last key-value pairs of obj of the same key replaces prev
- spread operator to copy over value
- Object.assign({}, a, new:key)
	- copy from right to left; all to first
