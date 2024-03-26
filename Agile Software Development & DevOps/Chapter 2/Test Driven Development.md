- Process in which test cases are written before the code that validates those cases
- Depends on repetition of a very short development cycle
- It is a technique in which automated unit test are used to drive the design and free decoupling of dependencies
- Following sequence of steps is generally followed:
	- Add a test
	- Run all test cases and make sure that the new test case fails
	- Write the code that passes the test case
	- Run the test cases
	- Refactor code
	- Repeat the above mentioned steps again and again
- Motto:
	- Red: Create a test case and make it fail
	- Green: Make the test case pass by any means
	- Refactor: Change the code to remove duplicate/redundancy

### Benefits
- Unit test provides constant feedback about functions
- Quality of design increases which further helps in proper maintenance
- Test driven development act as a safety net against the bugs
- Ensures that your application actually meets requirements defined for it
- Have very short development lifecycle

### Common Pitfalls
- Forgetting to run tests frequently
- Writing too many tests at once
- Writing tests that are too large or coarse-grained
- Writing overly trivial tests, for instance omitting assertions
- Writing tests for trivial code, for instance, accessorise
- Typical team pitfalls include:
	- Partial adoption
	- Poor Maintenance
	- Abandoned Test Suite

### Advantages
- Only write code that's needed
- More modular design
- Easier to maintain
- Easier to refactor
- High test coverage
- Tests document the code
- Less debugging

### Disadvantages
- No silver bullet
- Slow process
- All the members of a team got to do it
- Tests got to be maintained when requirements change
