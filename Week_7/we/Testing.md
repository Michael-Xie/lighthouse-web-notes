# Testing
- testing is about gaining **confidence** in the code we write
- different types of tests can be applied strategically to acheive a level of confidence that is hard to match with manual testing alone
- improves workflow

## Code Coverage
- metric to determine how many tests we have
- Istanbul
- shouldn't test implementation details, which is something that consumer of code doesn't do

## Regression Testing
- the process of verifying that previously uncovered bugs have not returned in all susequent versions of the software

## Automated Testing

## Types of Tests
1. Static
2. Unit
3. Integration **
4. End-to-End (E2E)

![alt LHL testing]("./images/LHL_testing.png")

- cheap to write (4 cheapest to 1 expensive)
- speed (4 fastest to 1 slowest)
- confidence coeff (4 lowest to 1 highest); simple prob to big prob
- integration tests provide the best balance of cheap, speed, problem
### Static Testing
- needs initial config, but very little maintenance

1. Linting
- ESlint and Prettier
2. Static Typing
- Typescript and Flow

### Unit Testing
- test a specific function or component in isolation
- Jest

### Integration Testing
- when different units of code are combined to create an application
- integration testing is the process of proving that tow or more units of code work together
- Cypress

## Test Driven Development
Goals of TDD by Kent Beck are:
1. Write new code only if an automated test has failed
2. Eliminate duplication

### Red, Green, Refactor
1. Red - Write a small test that doesn't pass
2. Green - Do the minimal amount of work to make the test pass
3. Refactor - Improve the code, continuing to ensure all tests still pass

### Battle-Tested Strategy
- remove ability to push code without a pull request
- all changes are peer reviewed and approved
- testing requirements
	- app builds successfully
	- all tests pass
	- coverage thresholds must be met for new code
	- coverage thresholds for the whole repo (maybe)
- quality guidelines
	- write easy to read code
	- avoid known problematic patterns (like == vs ===)
	- check for security vulnerabilities
	- eliminate duplicate code
- should **not** fail a pull request on style --> use prettier
- test and quality checks can be *automated*
	- linters and IDE plugins to help as code is written
	- Husky and Git ooks to check changes pre-push
	- TravisCI and Jenkins to build and test PRs
	- SonarCloud, Code Climate, Codacy for quality checks
	- Prettier to auto-fix code style
- PRs create a control flow
	- no force pushing
	- creates a place for automated tests to run
	- requires team participation
	- automated tests catch more edge cases **before** regressions happen
	- quality checks *minimize* technical debt and maintenace overhead
	- automating enforcement removes the need for a human code cop
	- include administrator checkbox (Github) for review, level playing field for all
	- peer reviews create opportunities to learn and share knowledge
- testable code is better code
	- cleaner separation of different functionality
	- fewer side effects (because mocking sucks)
	- better APIs because edge cases are tested for
- make the **right** thing the **easy** thing
- use built-in **coaching** to improve quality (Codacy, Code Climate)
- make the learning curve as **shallow** as possible
- keeping tested code tested is significantly **less hard**
- internal **training** is key; common understanding and usage
	- hackathons to add tests to older code
		- sprints where one person writes one test
	- hands-on workshops to teach testing techniques
	- cross-team code reviews to share knowledge
	- compile best practices into internal docs
	- coach the team on writing more testable code
	- hire external trainers if necessary
- don't forget: **executives** also need training
	- an untested product is *fragile*
	- fragile products break in unpredictable ways
	- unpredictability causes delays
	- delays cost oney and frustrate customers
- make code quality a point of **pride**
- **visually** represent code health in public (SonarQube)
- measure code health over time for teams
- make testing a **deliverable** not a "nice to have"
	- new features *without tests* are not safe to launch


## TLDR;
1. Write tests. Certain types of tests should be automated
2. Not too many. We don't need 100% code coverage to have a high level of confidence.
3. Mostly integration. These types of tests are more thorough and test how the different parts of the application work together.
4. Testing is essential, but comes with a cost. It is not optional. Repetitive testings can be automated. It will save time in the long run and test consistency will give us a higher degree of confidence.
