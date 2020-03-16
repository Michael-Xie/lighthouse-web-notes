# Intro to Ruby

## Common Commands
- `rvm`
- `which ruby` shows path of ruby command, which is thanks to the $PATH env variable
- `echo $PATH` provides an ordered list of directories where commands are searched 
- `irb` is the ruby REPL
- add ! to end makes function to replace original array
- The # is a convention to indicate that each is a method of an Array object; it is not a part of ruby syntax but instead a part of ruby documentation.

##
- speed is based on how concurrent code can be run at the same time

- rails has a gem called concurrency, which could increase its performance

What does exit(0) do?
On many operating systems a program can abort with exit(0), and the number passed in will indicate an error or not. If you do exit(1) then it will be an error, but exit(0) will be a good exit. The reason it's backward from normal Boolean logic (with 0==false) is that you can use different numbers to indicate different error results. You can do exit(100) for a different error result than exit(2) or exit(1).

## Blocks
If arguments are how we pass in data to methods, blocks are how we pass in behavior. Think of them as a chunk of logic that your method can run.

## Design Pattern: template method
In object-oriented programming, the template method is one of the behavioral design patterns identified by Gamma et al.[1] in the book Design Patterns. The template method is a method in a superclass, usually an abstract superclass, and defines the skeleton of an operation in terms of a number of high-level steps. These steps are themselves implemented by additional helper methods in the same class as the template method.

The helper methods may be either abstract methods, for which case subclasses are required to provide concrete implementations, or hook methods, which have empty bodies in the superclass. Subclasses can (but are not required to) customize the operation by overriding the hook methods. The intent of the template method is to define the overall structure of the operation, while allowing subclasses to refine, or redefine, certain steps.

## Constants
- `Math::PI` referes to a Math module with a PI constant
- First letter caps means constant
- :: means defined PI within the name space of Math

Capitalized words can be used to define a constant
A constant can refer to a Module, a Class or simple data like Floats and Strings
Namespacing is used heavily to limit the exposure of constants defined in the global namespace
The :: Syntax is used to access constants (Modules, Classes, etc)
It is convention to only capitalize the first letter when defining Class and Module constants like Apple
It is convention to capitalize and underscore the entire name when defining value constants like FOUNDED_BY


