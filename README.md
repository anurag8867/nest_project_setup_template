## Installation
# Directory Structure: [Click Here] (https://medium.com/the-crowdlinker-chronicle/best-way-to-structure-your-directory-code-nestjs-a06c7a641401)
```bash
$ npm install
```

## Running the app

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Test

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

```bash
command for new Module:
$ nest g resource users
```  

GuideLines: (Open for inputs)

Structure:
* controller -> service -> repo/db
* util(At component and root level)
* entity
* helpers
* dto

Product:
* UserService requires catService Function => UserService -> catServiceHelper -> catService(A Service should never calls its own helper)
* A Service should not call its own Helper function
* A helper can call its own service
* A service can call helper from other service
* Helper is for other service's help
* A controller should call only its own service

Node:
* https://www.tatvasoft.com/blog/node-js-best-practices/
* Try to use higher order function and avoid legacy for loop
* process manager pm2

Db:
* Sequelize ORM
* All calls to DB must hold transactions (Managed and UnManaged)
* Controller will be the best to start a transaction

Logging:
* what to log? error, warn, info, verbose, debug
* Controller, service and db. (Start of a function and end of a function)
* Winston is the most popular library
* Avoid Logging Sensitive Information
* We may link team/slack for system crash exception
* Automatically Log Uncaught Exceptions and Unhandled Promise Rejections

Typescript:
* Classes
* DataType definition
* Interfaces
* Inheritance
* Optional params must be the last params of functions/methods

Testing:
* Jest
* controller, service and db layer
* Unit test cases
* Integration test?(Question to Anubhaw)

Software Practices:
* Try to make variables as private as possible
* Put some common function into util folder
* Check existence of same function before creating new function
* Install eslint module in vs code
* SOLID Principle

Config Management:
* Config(Module) (Easy to maintain, but compromise with security, unwanted changes may go out)
* Secret Manager

Request Validation(General Validation):
* Class Validator
* Sync as well async validation
* custom validation (Decorator validation)

Questions:
* what is promise? object, associate handlers with asynchronous operation
* difference between object and class/prototype?
* is log async? console.log is sync.
* is reading a file async? .readFile, if we wanna read in sync readFileSync
* ensure all cores utilized? cluster module, even Ryan Dahl said the same thing in one of the google talk


* Need to research in respect to nest js
* Nest Js core module structure?