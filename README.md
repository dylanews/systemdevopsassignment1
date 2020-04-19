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

Integration-Testing:
- Integration testing is the phase in software testing in which the software modules are then to be combined and tested altogether as a group. It is used to evaluate the compliance of a system or component with specific functional requirements. Originally, in the script folder for integration-testing, there were no mocha reporters being mentioned. In the config.yml for circleci, there was also nothing mentioned in regards to hosting the nodes and the database.

e2e testing:
- e2e is a technique of testing that tests the entire softare product from the beginning to the end to ensure that the app runs as expected. It ensures that everything is working perfectly without any issues. In this assignment, we have used qawolf as the e2e testing tool which was lacking in the scripting folder. For the production script, there was also a lack of database details. In the config.yml for circleci file, nothing was mentioned in regards to running the scripts or database.

Explanation of solution:
Building the Docker Image:
- As mentioned, the Docker Image is a file consisting of multiplayer layers that allows the container to execute code. I have used the Docker image and implemented it as the image for circleci. Therefore, the docker image would always be used as an image and to help execute the container and the commands mentioned.

Running Tests - Unit Tests:
- In this project, As there was on specific javascript testing framework that has been mentioned in the script apart from the cross-env and the node-env. Therefore, I have added in an additional mocha/unit-test to specify and to apply the mocha testing framework to the application. In config.yml i have also specified the use of mocha unit-testing framework to test the application.

Code Coverage:
- The code coverage is used to report and to notify the users when any problems were to occur. For this pipeline, i have added the use of the nyc istanbul reporter allowing the application to be able to notify when any problems were to occur. With this, i have also added a reporter which would display the errors to the code-coverage to the users if any problems were to arise.

Linting:
- As mentioned above, in the script folder there was no lint framework specified. To solve this problem, I have attached Eslint as the framework and ./ allowing it to be able to perform through the whole directory. 

Integration-testing:
- For integration-testing, I have added the mocha reporter tool in the scripting folder and have also added in the proper processing commands in the config folder. The commands would ensure that the database will run properly with proper database environment variables. The integration-test is then ran with the node database modules and then to be performed.

e2e testing:
- For e2e testing, as it is a full rundown of testing from the beginning of the software till the end, qawolf would then be used as the tool to perform the e2e testing. In the script file, there was a lack of what tool to use in the e2e-testing script, therefore, i have added the npx qawolf which would allow the qawolf tool to be used. In the production script, there was also a lack of user, passwords and host details which was then added to ensure that the database would be able to be connected. In the config.yml file for circleci, i have added the required environment and commands in order to allow the pipeline to be able to install and run the e2e testing without any trouble.

SCREENSHOT OF CIRCLECI AND GITHUB:
![screenshot](https://github.com/s3699661/systemdevopsassignment1/screenshotcircleci.png)


MULTIPLE FAILURE SCENARIOS:
![fail scenario 1](https://github.com/s3699661/systemdevopsassignment1/failscenario1.png)
![fail scenario 2](https://github.com/s3699661/systemdevopsassignment1/failscenario2.png)
![fail scenario 3](https://github.com/s3699661/systemdevopsassignment1/failscenario3.png)
![fail scenario build 4](https://github.com/s3699661/systemdevopsassignment1/failscenariobuild4.png)

INTEGRATION TEST FAIL LOG -
- The reason behind the integrationt-test build failure is due to the missing script from the node_module as there were no node modules being used. 
- *See console fail log in file*

QAWOLF TEST FAIL -
- The reason behind why the qawolf test failure is because there is no database hosted. Therefore the application was not able to test as they were not able to run the software at all.
![qawolf fail 1](https://github.com/s3699661/systemdevopsassignment1/qawolf1.png)
![qawolf fail 2](https://github.com/s3699661/systemdevopsassignment1/qawolf2.png)

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

DONE

## Running Tests

DONE

### Unit tests

DONE

There are [Mocha](https://mochajs.org) based unit test in the application. 

### Linting

DONE

### Code coverage

DONE
### Integration tests

Integration tests are implemented using Mocha as well. 

DONE

### End to end test

E2E tests are implemented using QaWolf and requires a database backend to execute properly.

Set the environment variable `QAW_HEADLESS` to true to run the e2e in headless mode

https://www.qawolf.com/

DONE