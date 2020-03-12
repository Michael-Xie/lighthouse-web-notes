# Object Oriented Programming

## OOP Goals and Good Practise
1. Abstraction
2. Public vs Private 
	- prefix with _ for variable names for JS, as this feature doesn't exist in JS
3. Single Responsibility Principle
- a class should be responsible for a single part of the app's functionality, giving it only one reason to change. It should have only one job!  
4. Inheritance

## Javascript
- used prototype prior to ES6
- after ES6, there is the introduction of classes
- there is NO right way for OO in JS

## Dependency injection
- Passing an object the things it needs rather than having the object access them itself"

## `this` and `bind`
- `bind`
- `this`

object bundled with properties and functions
```
let dog = {
	sound: 'woof',
	talk: function() {
		console.log(this.sound)
	}
}

dog.talk() //"woof"
let talkFunction = dog.talk
let boundFunction = talkFunction.bind(dog)
boundFunction() // "wolf" if not bind then talkFunction cannot connect to dog as `this` only refers to where it is at when called. Since function is outside object, this is undefined
```
