# Unit and Integration Testing
- debugger added to code, and will have access to all variables loaded up to that point in browser console

- tests are needed so ensure app doesn't break later down the road

## dom-testing-library
- A *query* is a combination of a query variant and a query type.
- ie. for *query* we want ot use getByText. The variant is getBy and the type is ByText

## continuous integration (CI)
- tests run after each commit

## helpful commands
- `xit` or `test.skip` to skip the test
- `it` and `test` are interchangeable; stay consistent in usage
- `p` to choose a specific file in watch mode, then specify the file name

## mock functions
This reading provides a rapid introduction to the concept of mock functions. We are going to use jest.fn to poke holes in reality as we continue to write more sophisticated tests. There are two primary uses of mocks that we will explore to learn unit and integration testing.

1. We can capture the different calls made to the function and the arguments for each call.
2. We can configure the function to return any value that we want for the specific test.

When we use getByText we should be confident that the element exists. If it does not exist, then it throws an error instead. We can test for the absence of something by using queryByText and checking that the value is null.
It is a case insensitive regular expression. This search is more general than the absolute string "Student name cannot be blank".
The onSave reference is a mock function that we can pass to the Form component.

## Code coverage
Code coverage only provides a measure of how many lines of code run in a program, not how well tested the behaviour is.

npm test -- --coverage --watchAll=false

## Fixture
The term fixture can be used to describe reusable static data that is imported or embedded into a test file. We need to make sure we have accurate data that matches the schema from the server.

## await async
The await keyword can only be used within an async function. Trying to use it at the top level of a node module will result in a SyntaxError.

ByLabelText, ByPlaceholderText, ByText, ByDisplayValue, ByAltText, ByTitle and ByRole
