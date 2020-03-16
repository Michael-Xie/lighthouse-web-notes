# TDD - Ruby
- given a legacy without TDD in space
- some tests in place
- fix something and deploy and other bugs come out again

## how to tame legacy code

- deploying without tests is flying blind
- the ideal time to write tests is now

- to be tested, needs to be refactored
- any new code **must** have tests
- bugs in code must be **reproduced** with a testa
- use **test** to learn legacy code
- test last leaves holes in test coverage
- write a failing test -> make test pass -> refactor (RGF)
- never write **new functionality** without a **failing test**

- every line of **tested** code is **reliable** code
- every line of untested code is **unreliable** code
- tests **prevent** breaking
- tests are **documentation**
- test driven code is modular, loosely coupled, small methods
- tests remove **fear**

- if code interacts with API, use mocks and stubs
- a stud is a stand in for an object called by your code
- mocks are "stubs with attitude"

- testing is evolving
- TDD is developing beyond yourself

## EDD
- bin/rail c 
goes to console
can use active record to create entry
Sale
Sale.count
Sale.create! name: "X-max Sale!", starts_on: 'Dec 5, 2019', ends_on: 'Jan 3, 2020', percent_off: 50
