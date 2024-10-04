# TDD BDD Unit Testing

# The TDD Cycle

RED: Write a test that fails (becouse the feature isn't implemented yet)

GREEN: Write just enough code to make the test pass 

REFACTOR: Clean up the code without changing its behavior (does it still pass the tests after the refactor?)

### Benefits of TDD

-Ensures code reliability and fewer bugs
-Forces developers to clarify requirements early (Build up the logic)
-Encourages simple, maintainable code
-immediate feedback on code quality
-Facilitates refactoring without fear of breaking the system

## TDD in Python

Python provides tools that facilitate TDD:

- unittest (Python's built-in module)
- pytest (more user-friendly, with powerful features)

Python's dynamic nature makes writing and running tests easy and fast

## Writing Tests with unittest

Each test case is a method inside a class derived from unittest.TestCase

```
import unittest

class TestMath(unittest.TestCase):
    def test_addition(self):
        self.assertEqual(1 + 1, 2)

if __name__ == '__main__'
    unittest.main()
```

## Writing Tests with pytest

No need for test classes; tests are simple functions (but they can be grouped in classes if needed)

Can use assert statements for tests

Includes fixtures, parameterization, and custom plugins.

```
def test_addition():
    assert 1 + 1 == 2
```
```
pytest # run tests using pytest in the command line
```

### Coverage

Coverage indicates the percentage of lines of code in our codebase that are executed during unit testing.

Code coverage and test quality aren't directly related (one can achive 100% test coverage and still have bugs) but it's a good indicator about which parts of our code aren't being tested at all.

## Common Patterns in TDD

### Mocking

Simulating complex external dependencies without needing them during testing(i.e.: databases, other microservices, expensive API calls, ...)

### Edge Cases

Writing tests for boundary and edge cases

### Regression Testing

Running all the tests when further developing our codebase(or fixing bugs)

Do the new changes break existing functionality(regression)?

### TDD Challenges

- Initial overhead of writing tests
- Tests can become brittle if not maintained
- Difficult to test UI or complex interactions
- May slow down rapid prototyping


### TDD Best Practices

- Write small, focused tests
- Test both "happy path" and edge cases
- Refactor tests as well as code
- Use Continuous Integration (CI) to run tests automatically

### Example TDD Workflow

1. Write a failing test for a small piece of functionality
2. Write the minimum code necessary to make the test pass
3. Refactor both the test and code for readability/efficiency
4. Repeat the cycle

# BDD (Behavior-Driven Development)

An extension of TDD focused on testing behavior from the user's perspective.

Goal: Create shared understanding among developers, testers and non-technical stakeholders.

Specification by Example: Uses examples to describe how software should behave.

Know what our clients whant and do not want

### Define a Behavior

Collaboratively write behavior scenarios using examples.

### Automate the Scenario

Convert the behavior into automated tests

### Implement the behavior

Write code to fulfill the behavior, running tests to ensure correctness.

# BDD VS TDD

TDD: Focuses on the technical implementation (unit tests).

BDD: Focuses on the system's behavior from the user's perspective (higher-level tests).

# BDD with Python

Popular Python tools for BDD:

behave: A BDD framework using Gherkin syntax for writing scenarios.

pytest-bdd: Pytest plugin that enables Gherkin-style feature files.

```
Feature: Title of the feature

    Scenario: Title of the scenario
        Given some context
        When an action is taken
        Then an outcome is expected
```

Example:
```
Feature: User login

    Scenario: Successful login
        Given the user is on the login page
        When they enter valid credentials
        Then they should be redirected to the dashboard
```

### Benefits with BDD

Enhanced collaboration

Align technical and non-technical team members.

Clear requirements

Example-based approach ensures better understanding of requirements.

Living documentation

Gherking scenarios serve as both documentation and tests.

User-Centric Testing

Focuses on user experience and business value.

Challenges of BDD

Requires upfront time for collaboration.

Maintaining scenarios and tests can be challenging as systems evolve.

May lead to over-specification if not balanced properly.

### BDD Best Practices

Involve stakeholders

Ensures collaboration between all parties (business, QA, devs).

Start small

Begin with critical features before expanding the entire systems.

Keep scenarios simple

Write clear, concise scenarios than describe behavior, not implementation.

Test early and often

Continuosly run BDD scenarios to catch issues early.

### Example BDD Workflow

Identify a feature

Work with stakeholders to determine behavior.

Write scenarios

Collaboratively create feature files with clear scenarios.

Write steps definion

implement Python functions to automate the steps.

Run tests

Execute the tests, write code to pass them, and refactor as needed.

