Assignment 1 System deploymand and Operations

Name : Eng Wen Shing

Student ID : s3699661

Analysis of the problem:
Building the Docker Image:
- A Docker image is a file, comprosing of multiple layers that allows the container to execute code. An image is essentially the complete and executable version of the container. There was no image and no container in the original code, there was only configuration between each script, dependencies and code. 

Running Tests - Unit Tests: 
- Unit-testing is a software method which involves testing individual units of source code which usually involves one or more lines of code. There was test files and test scripts inside package.json and the test folder, but there was no specific javascript testing framework that has been mentioned in the script. There was only mocha dependencies that was being called in the package.json folder.

Code Coverage:
- A test coverage is a measure that has been used to describe and to report the degree in which the source code of the program is being executed. It would cover and compile the source code of the progam and then be reported. Originally in the pipeline, there was no reporter or code coverage that was being mentioned or done. 
- In the code coverage section of package.json, there was also no reporter specified which is a problem as without a reporter, details of the code-coverage would not be able to be displayed.

Linting:
- Linting is a tool that analyses source codes and to report or notify any bugs, errors, or suspicious constructs. In this program, there was a test-lint script that has been provided but there was no framework mentioned.

Explanation of solution:
Building the Docker Image:
- As mentioned, the Docker Image is a file consisting of multiplayer layers that allows the container to execute code. I have used the Docker image and implemented it as the image for circleci. Therefore, the docker image would always be used as an image and to help execute the container and the commands mentioned.

Running Tests - Unit Tests:
- In this project, As there was on specific javascript testing framework that has been mentioned in the script apart from the cross-env and the node-env. Therefore, I have added in an additional mocha/unit-test to specify and to apply the mocha testing framework to the application. In config.yml i have also specified the use of mocha unit-testing framework to test the application.

Code Coverage:
- The code coverage is used to report and to notify the users when any problems were to occur. For this pipeline, i have added the use of the nyc istanbul reporter allowing the application to be able to notify when any problems were to occur. With this, i have also added a reporter which would display the errors from the code-coverage to the users if any problems were to arise.

Linting:
- As mentioned above, in the script folder there was no lint framework specified. To solve this problem, I have attached Eslint as the framework and ./ allowing it to be able to perform through the whole directory. 

-# Express Example

This repository demonstrates the usage of Sequelize within an [Express](https://expressjs.com) application.
The implemented logic is a simple task tracking tool.

## Configuration

Configuration can be found in `config/config.js`

### Environment vaiables used to configure the application

- DB_USERNAME - username for the database server
- DB_PASSWORD - password for the database server
- DB_NAME - name of the database
- DB_HOSTNAME - hostname of the database server

## Starting App

*Without Migrations*

```
npm install
npm start
``
**With Migrations**

```
npm install
node_modules/.bin/sequelize db:migrate
npm start
```

This will start the application and create an sqlite database in your app dir.
Just open [http://localhost:3000](http://localhost:3000).

## Building the docker image

TODO

## Running Tests

### Unit tests

There are [Mocha](https://mochajs.org) based unit test in the application. 

### Linting

TODO: add ESLint command

### Code coverage

TODO: Add istanbul(nyc) commands

### Integration tests

Integration tests are implemented using Mocha as well. 

TODO: set up integration test environment and run integration tests


### End to end test

E2E tests are implemented using QaWolf and requires a database backend to execute properly.

Set the environment variable `QAW_HEADLESS` to true to run the e2e in headless mode

https://www.qawolf.com/

TODO: Set up e2e test environment and run the e2e tests