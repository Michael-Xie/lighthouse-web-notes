# Advanced Topics

## ESx
- 2009 ask ES5
- 2015 aka ES6
- 2016
	- `array.prototype.includes`, indexOf can't find NaN
	- `2**2`, same as Math.pow(2,2) for exponents
- 2017:
	- async
	- trailing comma
		- run `git blame` and ask that person for help
		- messes up history if in a list someone adds to the end and needs to add comma; now you can have a comma at end and still not throw error
	- string padding
		- `<string>.padStart(<pad size>, <padding char>)`
		- `<string>.padEnd(...)
	- async, await
	- object.entries
- 2018:
	- looping promises
		- `async function ... for await (const obj of promises) {...}`
		- await Promise.all(promises) // wait for all to finish then moves on
	- rest (always at end of operator): destructuring `const {firstName, lastName, ...remainder} = person; // remainder is a an object // also use for array		- can also be used to throw out things not needed and keep remainder
	- spread (usually before comma) 
- 2019:
	- bigint to handle larger numbers
- 2020: 
	- global `this`
	- optional chaining
		if(person.friends?.scott?) vs if (person && person.friends && person.friends.scott)


## Design Thinking
- project mgmt
- planning
	- notion
	- basecamp
	- github projects
- async communication
- figma -design tool
- not re-invent the wheel, use lib
	- react component library, like material ui and ant design, tailwind

- divide by feature stories

- conferences
- professional development budget: e-learning budget, conf
- peaks and valleys - UX designer from shopify article
