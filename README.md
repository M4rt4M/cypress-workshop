# Cypress Test Writing Fun - Outline

## Contents
1. Set Up
2. Running The App
3. Running the Tests
   1. Within the command line
   2. Within the test runner window
4. The Task


### Set Up
These are assuming you already have [yarn](https://classic.yarnpkg.com/lang/en/docs/install/#mac-stable) installed on your machine. If you don't, ask for help with this part. 

1. Install Dependencies

Open the terminal/command line and run `yarn install`

2. Check Cypress has been installed

Within the command line run `cypress --version` and check you get something similar to
```
Cypress package version: 9.5.4
Cypress binary version: 9.5.4
Electron version: 15.3.5
Bundled Node version: 16.5.0
```
If there is an error about cypress not being there, run
```
npm install cypress --save-dev
```

### Starting the Application

**To run the tests we need to start the app** by running `yarn start` and you should see something like this afterwards
```
yarn run v1.22.18
$ http-server -p 8888 -c-1
Starting up http-server, serving ./
Available on:
  http://127.0.0.1:8888
  http://192.168.0.18:8888
Hit CTRL-C to stop the server
```

Now you can head to [http://localhost:8888/](http://localhost:8888/) and (hopefully) you will see a swanky todo app running in the browser.

### Running the Cypress tests

N.B. _do this in a separate terminal to the one that you used to start up the application._

There are two ways to run the Cypress tests, these are firstly in the background and have the results printed out to your terminal or via the test runner window. The former is useful for running existing tests and for when writing simple tests that you're confident will work how you intend them to. The latter is good for when you're writing tests and want to see them running to check they're working as expected. The commands to run them are
> Run tests in background:
>`yarn cypress run`

> Run tests with the test runner window:
>`yarn cypress:open`

For more information about the test runner window you can look through [Cypress' docs](https://docs.cypress.io/guides/core-concepts/test-runner#Overview).

### The Task

#### Part One - Fill in the Blanks

Head over to [**task-one.spec.js**](cypress/integration/practice/task-one.spec.js). In here you'll find a test suite written by a very lazy tester (me). Your task is for each test, read the title and then complete the body to get the tests passing. 

If there's any tests that will require a specific cypress command then I've added them as comments within the tests with a link to the docs but for any other issues, just ask for help. 

There's some commands that you will be using frequently and I've added a list of these, along with a description and link to the docs, which can be found in [**common-cy-commands.md**](common-cy-commands.md).
