---
layout: post
title: "Client Overview"
date: 2021-11-21 22:22:20 -0500
author: "Team G"
---
### SYSTEM OVERVIEW
*Specifications*
BigWords is built using the following architecture:
- Languages: Javascript, React.js
- Backend Service: Firebase Cloud Functions
- Deployment Service: Firebase Hosting
- Database: Firebase Real-Time Database

*How Architecture Works*
The front-end for BigWords is written with React.  This code, when deployed by Firebase hosting, will build the website which users can interact with.

BigWords supports access from two different types of users, end users and admin users.  End users will be the regular caretakers who will be using the application.  These users will interact with the web content though the Firebase hosted app.  This user input will be passed to React, which will send this information to the Real-time database.  Within the database, user input will write and change the data pertaining to their account and experience.

Admin Users are those who will be servicing the website by adding and updating book information.  Using Firebase Cloud Functions, Admin Users can input new book information that will be processed and written into the Real-Time Database.  This information will then be used to populate data into react and displayed on the front-end of the application.

For a visualization of this, view the [architecture diagram](https://drive.google.com/file/d/1xZ34oV8ZcmgT-18Jw9oZuGVB4lBdZqQu/view)

### WEBSITE ACCESS
*Accessing Codebase*
The codebase for BigWords is located at the link below.  This project is currently private.  In order to access the project, please email one of us and we will add you to the contributors list.
https://github.com/jackowfish/big-words-app 

The code for the Book Parser created to format book data for Firebase’s real-time database is located at the link below.
https://replit.com/@jackowfish/Book-Parser#index.js 

*Accessing Database*
The hosting and database for BigWords is through Firebase.  To access this project, click the link below and log in using the bigwordsweb@gmail.com credentials.
https://console.firebase.google.com/u/2/project/bigwords-202f6/overview

*Accessing Live Website*
The live version of the BigWords website can be found at the link below.  This link is currently public and accessible to everyone. If you are accessing the website on desktop, it is best viewed through your browser’s developer tools with iPhone dimensions.
https://bigwords-202f6.web.app/#/. 

*Admin Access on Website*
Admin accounts on BigWords allow access to the “Add Book” tab.  This tab allows admins to add new books into the database.  To grant your account admin status, please email one of us and we will update your account settings.

### COST
BigWords currently uses Firebase for Hosting, Database, and Cloud functions on the Blaze plan.  This plan is for projects that require capabilities provided by the paid services.  This plan allows us full usage of free Firebase products and features, free-usage quota for Firebase products, pay-as-you-go pricing for any additional usage of paid Firebase products, and access to paid Google Cloud products and features.

Each month, Firebase starts free until your project exceeds the free-usage quota.  For more information on monthly costs, visit
https://firebase.google.com/pricing 

For more information about Firebase’s pricing plans visit https://firebase.google.com/docs/projects/billing/firebase-pricing-plans

### PROGRESS
The table below shows the progress we have made on the “need-to-have” components described on the [user stories](https://jackowfish.github.io/big-words-site/2021/09/12/User-Stories.html) page as of 11/21/21. Currently, no “nice-to-have” components have been implemented.

|  Component | Status  |
|---|---|
| As a caregiver, in order to start tracking my children’s words, I can create an account and input personalized information like date of birth and name for both caregivers and children. I can also authenticate multiple caregivers and children on the same account.  |  Completed |

| As a caregiver, in order to personalize my account, I can always add/edit/remove caregivers and children, as well as any relevant information. I can also change my password when needed.  |  Partially Completed Updating password not yet implemented|

| As a caregiver, in order to organize books I have read to my children, I can indicate which caregiver read each book and to which child.  |  Partially Completed Components accessible through application, but still need to be connected to the database |

|As a caregiver, in order to find books to read to my children, I can search for books within the database based on title and specific words/big words.   | Partially Completed Components accessible through application, but still need to be connected to the database|

| As a caregiver, in order to keep track of books I have read to my children, I can access a list of books I have logged and see how many times I have read it and the words each book contains. I can also see books that contain similar words to those books I have read.  |Partially Completed The number of times a book has been logged is tracked within the database, but not displayed within the application.|

| As a caregiver, in order to save books that aren’t already included in the app, I can fill out a form with the title, author, and/or picture of the book. Once the form is submitted, a BigWords admin will be notified to add the book to the database.  | Partially Completed   |

| As a caregiver, in order to track my children’s exposure to words, I can view the words and big words my child has been exposed to in a personalized dictionary.  |Partially Completed Users can view words and big words they have logged, “by child” sorting needs to be implemented|

| As a caregiver, in order to gain more knowledge about preparing for a child’s future and the benefits of reading to them, I can access various relevant articles.  | Not Started  |

| As a caregiver, in order to notify BigWords of any issues with the app, I can fill out a form that will be sent to the BigWords team.  | Not Started  |

### NEXT STEPS
With the current state of BigWords, we believe the next highest priority would be to finish all incomplete “need-to-have” features and begin transferring all book data into the Firebase Database.


