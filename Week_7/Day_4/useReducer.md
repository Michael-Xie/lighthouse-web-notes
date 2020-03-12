# useReducer

- similar to array's reduce function
[1,2,3,4].reduce((acc,val) => [...acc, val*val], [])
same as map

define outside of component to not on component's state and might cause re-render when changed

```
const reducer = (prevState, action..


in componenet
const [state, dispatch]
```

if you want to change something, make a copy.
if reducer returns same object, then React won't both to re-render
this results in page not updating

## Websockets

ws://localhost:8888 -insecure
bwss
