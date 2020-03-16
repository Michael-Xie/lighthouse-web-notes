# React and Data Fetching

## Hooks
- relatively new way to use react
- used to use class syntax, class-based componenets
- moving to functional based components

## Functional Reactive Programming
- like excel where a change in one cell, has chain of changes to associated cells

##
- DOM changes are costly time operation
- React has a virtual DOM, where change in component doesn't immediately apply to DOM
- can update once per 60frames, not conceivable by human eyes

##
// gets the most current value and add one
setValue(value => value + 1)
// value from last render value, and waits for more changes
// so below will be equivalent to having just one statement 
setValue(value + 1)
setValue(value + 1)

set<blah> tells react that something is being changed and signals to re-render

## Rule to Hooks
- Do **not** manipulate variables from useState
- correct way: setStuff(stuff => [...stuff, Math.random()]);
- give a function to a setter, the safe way
1. Don't call Hooks inside loops, conditions, or nested functions
	- ie. if you want to pass a condition before executing the hook (useEffect) then put the condition inside of hook, instead of wrapping around the hook
2. Only call Hooks from inside React componenets
3. The effect method that we pass to useEffect must either return undefined or a function
	- for use to clean up

## useEffect
- a hook
- for general things outside of React
- can be dependent on a change of array of variable(s)
- replaces the life cycle method in older React code
- can use for clean-up, where useEffect returns a function when main function is done
- make ajax request or can use axios(supports IE), fetch(does not)

```
useEffect(function, [])
[] - values
apply effect when values changes between re-renders
```
### sequence
1. React: Run all component funcitons to generate React element tree. Store effect functions for after paint. Apply changes to the DOM.
2. Browser: Paint the required elements based on current DOM
3. React: Run all effect functions submitted during render

### Classes
similar to useEffect but uses lifecycle method
- componentDidMount
- componentDidUpdate
- componentWillUnmount

make initial request in ComponentDidMount, when component updates, componentDidUpdate gets called. Within ComponenetDidUpdate, check if "term" has changed. If it did, then make API request.

## Selector
- a function that accepts state as an arg and returns data that is derived from that state
- ie. filter results
