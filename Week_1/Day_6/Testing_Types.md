[Table Of Contents](../../README.md)

# Unit Testing, Integration Testing and Functional Testing?

Finding your way around the maze that is JavaScript testing can sometimes be difficult. There are unit tests, integration tests, functional tests, E2E tests, browser tests… With so many buzzwords, who knows what they do and which one to use, what for, and when?

## Unit Testing 

Unit testing is the practice of testing small pieces of code, typically individual functions, alone and isolated. If your test uses some external resource, like the network or a database, it’s not a unit test.

# Integration Testing

As the name suggests, in integration testing the idea is to test how parts of the system work together – the integration of the parts. Integration tests are similar to unit tests, but there’s one big difference: while unit tests are isolated from other components, integration tests are not. For example, a unit test for database access code would not talk to a real database, but an integration test would.

# Functional Testing

Functional testing is also sometimes called E2E testing, or browser testing. They all refer to the same thing.

Functional testing is defined as the testing of complete functionality of some application. In practice with web apps, this means using some tool to automate a browser, which is then used to click around on the pages to test the application.