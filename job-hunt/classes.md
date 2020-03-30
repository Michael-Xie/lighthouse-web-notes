# Classes
- [reference](https://github.com/getify/You-Dont-Know-JS/blob/1st-ed/this%20%26%20object%20prototypes/ch4.md)
- Classes are a design pattern 
- Key Characteristics
	- inheritance
	- polymorphism

- **Classes mean copies.**

When traditional classes are instantiated, a copy of behavior from class to instance occurs. When classes are inherited, a copy of behavior from parent to child also occurs.

Polymorphism (having different functions at multiple levels of an inheritance chain with the same name) may seem like it implies a referential relative link from child back to parent, but it's still just a result of copy behavior.

- Javascript specific
	- can't copy to instantiate, instead mimicks the behaviours using mixins
	- Mixins takes the source object and target object, adds any missing properties and methods from source to target, and returns target
		- functions are not copied per se, but references to them are
	- can't do relative polymorphism
		- need absolute reference
		> But if we said Vehicle.drive(), the this binding for that function call would be the Vehicle object instead of the Car object (see Chapter 2), which is not what we want. So, instead we use .call( this ) (Chapter 2) to ensure that drive() is executed in the context of the Car object. 
		- above can be explained by mixin behaviour, where Car and Vehicle have the same method drive, therefore drive from Vehicle is not carried over and called  Explicit pseudo-polymorphism, which should be avoided wherever possible, because the cost outweighs the benefit in most respects.
