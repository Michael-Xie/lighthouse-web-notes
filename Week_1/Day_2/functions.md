# Functions

- Break parts into concepts to become functions
- Functions should have an easy to understand name for others to read and figure out code
- A useful principle is to not add cleverness unless you are absolutely sure you’re going to need it. 
It can be tempting to write general “frameworks” for every bit of functionality you come across. Resist that urge. 
You won’t get any real work done—you’ll just be writing code that you never use

## Naming Conventions
- avoid generic names like 'data', or 'run'
name your functions beginning with action words like createUser, or sendUserData
be consistent with your naming conventions
if you're joining an existing project, observe and adapt any existing conventions

Here are all 5 rules reviewed below:

1. Give your functions precise verb/action based names
2. Use camelCasedNames (like this one)
3. Properly indent the function code
4. Functions should focus on a single task: returning a value or causing a side effect. Break your function into additional smaller functions if you find it doing two or more things
	-  One single task could be to compute and return a value (eg: zeroPad)
	- Another single task could be to perform a side effect such as logging a message to the screen (eg: printFarmInventory)
5. Data needed by Functions should be passed in as parameters/arguments (i.e. local scope) instead of being accessed directly
