---
layout: post
title: "Test Coverage Report"
date: 2021-11-08 20:21:20 -0500
author: "Team G"
---

[Test Coverage Report](https://github.com/jackowfish/big-words-app/commit/d0d13a235f0d1917841bcdd4c46cefbcd3f26a3b)

This test coverage report is intended for the sections of our web application that are ready to be tested.  This includes: book uploads, login, signup, signout, and maintaining authentication veracity.  To achieve this we used cypress for end-to-end testing and Vite as our web packer.  As we continue to develop the BigWords website, we plan to update the test suite.  While developing our tests, we found that Vite did not have instrumentation packages that worked concurrently with Cypress.  This required us to determine how to instrument the code to work with Cypress ourselves.  Although we are testing to ensure our components and hooks are functioning properly, we are still yet to find out how to get the code coverage aspect to work.

The gold standard for testing as discussed in class declares: “an app with automated tests [should cover] all of the important features”.  In the current state of our code, our priority is to maintain authentication veracity.  The core concept of our application is for caretakers to quickly and accurately log books they have read to their children.  Testing to ensure users have secure access to their account while using the application is the first step to achieving this.  Maintaining authentication, alongside testing our login and signup form, gives us confidence that these features are functioning correctly.  However, as we continue to build upon our application, additional features including logging books and updating account information will also be tested.  

Due to the limited features of our application, we believe that a majority of our code should be tested, however, some code should be tested more rigorously than others.  For example, code connected to static pages or simple components should only be tested to ensure they were rendered properly.  Meanwhile, code connected to handling user events, especially those related to reading and writing information to our database, should be tested extensively.

Overall, our current results represent a suite well on its way to being a healthy one.  Although we are still working on getting our code coverage to work, the tests we have written should give us confidence that these features of BigWords are functioning properly. Hopefully with this base in place, we may begin to create a feedback loop which will help both our application and its test suites grow stronger.