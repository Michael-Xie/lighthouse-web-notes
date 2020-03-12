# React - Component UI

- Components are just functions
- props(Object) -> returns JSX
```
const Header = () => {
	return <h1> Hello World </h1>
}

<Header/>

// props children

const Header = ({children}) => {

}
```
OR
```
const Header = (props) => {
	const {children} = props;
}
```
**children is array-like but NOT array** SEE documentation to iterate over etc

JSX -> babel -> JS
```
React.createElement(Header, { className: 'my-cool-header'},
	React.createElement('span', null, 'Hello, world!')
)
```
null means no props passed to span

## State
- functional programming

const Counter = () => {
	return (
		<div>
			<button>-</button>
			<span>0</span>
			<button>+</button>
		</div>
	)
}

NOTE: Install React devtools

