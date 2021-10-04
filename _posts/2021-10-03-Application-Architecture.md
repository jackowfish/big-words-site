---
layout: post
title:  "Application Architecture"
date:   2021-10-03 21:48:00 -0500
author: "Team G"
---

**List of Architectural Designs**

* Languages/Libraries: *Javascript, React.js*
* Backend Service: *Firebase Cloud Functions*
* Deployment Service: *Firebase Hosting*
* Database: *Firestore*

**Javascript**

*Summary*: In order to create a responsive web application, we decided to use Javascript.

1. *Problem*: For our application, we need a language that will be responsive to user and admin input as well as store and retrieve information from a database. The purpose of BigWords is for caretakers to access and record the books they have read to their children regardless of where they are. This language should reflect this and be able to function on both mobile and desktop browsers.
2. *Constraints*: Our client is looking for a web-based application. In their initial pitch, our client suggested Java as a preferred language for this project. Although preferred, we have been given the freedom to choose whichever programming language we believe to be fit for this project.
3. *Options*:
   * Javascript
     * Pros: cross-platform language, executed in browser, dynamic type-checking, mainly used for web-apps, works side-by-side with HTML and CSS, compatible with Firebase/Firestore and React.js
     * Cons: enhanced security would require additional effort
   * Java
     * Pros: mainly used for desktop/mobile apps, allows better security
     * Cons: May take longer to develop, user interaction may be slower
4. *Rationale*: We decided to use Javascript since it is a lightweight, cross-platform programming language that allows web pages to be dynamic and interactive. Javascript is also compatible with React.js and Firebase/Firestore, the framework, hosting, and database service we plan to use while developing BigWords.

**React.js**

*Summary*: In order to create a dynamic user interface, we decided to use React.

1. *Problem*: For our application, we need a way to build an easy to navigate UI that can accept data in a fast, scalable, and simple way. While using BigWords, users should be able to create and edit their account as well as search for and log books at the press of a button.
2. *Constraints*: Our client is looking for a web-based application. In their initial pitch, our client suggested Java as a preferred language for this project. Although preferred, we have been given the freedom to choose whichever programming language we believe to be fit for this project.
3. *Options*:
   * React.js
     * Pros: Declarative, Component-Based, render with Node.js and on mobile apps with React Native, supports server-side, can be used with other frameworks, familiarity among group members.
     * Cons: may require use of additional libraries for routing
4. *Rationale*: We decided to use React because it is an open-source, declarative, component-based framework that will allow us to create dynamic user-interfaces. By using React, we will be able to quickly receive input from our users and quickly store/retrieve this information within our database. React can also be used cross-platform, meaning we will be able to develop for browsers on desktop and mobile.

**Firebase Hosting** 

*Summary*: In order to deploy our website, we decided to use Firebase Hosting.

1. *Problem*: We need a way for BigWords admins and users to access the application. BigWords will also be built as a responsive web application, which will be able to support static and dynamic content.
2. *Constraints*: Our client wants users to access BigWords easily from their web browser either from their personal computer or mobile device, regardless of where they are. Creating BigWords as a desktop or iOS application may prevent potential users from accessing the application. Our client is also developing BigWords as a passion project. Although we have not discussed whether or not our client would be willing to pay for hosting, at this time free hosting of the application would be preferred.
3. *Options*:
   * Firebase
     * Pros: Free tier, access to Cloud Functions and Firestore, used for both static and dynamic content, experience using Firebase among teammates.
     * Cons: may need to change to a paid tier depending on usage
   * Heroku
     * Pros: Free tier, Postgres, Redis, and Apache Kafka data services, app-centric approach for software delivery, supports multiple languages.
     * Cons: may need to change to a paid tier depending on usage, unfamiliarity using Heroku among teammates.
4. *Rationale*: We decided to use Firebase Hosting since it is a free, secure, fully-managed hosting service for static and dynamic content as well as microservices. Firebase also has seamless integration with cloud functions and Firestore, a flexible, scalable NoSQL cloud database to store and sync data for client- and server-side development.

Firebase Cloud Functions

*Summary*: In order to allow our user to easily input book data to our database, we decided to use Firebase Cloud Functions.

1. *Problem*: We need to create a way for our client to easily input book information that will be sent to our Firestore database as books are requested to be added to the application by users. This would include book data like title, author, words, big words, etc..
2. *Constraints*: Our client wants users to be able to request books and have them added to the database. Having our client input each requested book will still take time so requests by users cannot be processed instantly.
3. *Options*:
   * Firebase Cloud Functions
     * Pros: already know this works well with other options we chose for hosting and database
     * Cons: unfamiliarity with firebase cloud functions so will be a learning curve
4. *Rationale*: We chose Firebase Cloud Functions because we are already using Firestore for our database and these are both part of the Firebase platform and already often used together. It is low maintenance, secure, and will provide our client an easy way to input any new data to the Firestore database as needed.

**Firestore**

*Summary*: In order to store user and book data, we decided to use Cloud Firestore.

1. *Problem*: For our application, we need a place to store a large amount of book data that users can frequently access, as well as information regarding each particular user. Data will constantly be added by the client so the database will be updating often.
2. *Constraints*: Firestore is free to start, but if more quota is needed than provided at the free tier, then there will be a cost. This will hopefully not be a problem with the amount of book data we are inputting, along with user data
3. *Options*:
   * Firestore
     * Pros: Will work well with Firebase Hosting and Firebase Cloud Functions, has a free tier, team members are familiar this this
     * Cons: may need to change to a paid tier depending on usage
   * AWS
     * Pros: has a free tier, also twelve months free for paid tier
     * Cons: not easily used in tandem with our other choices for hosting and such, may need to change to a paid tier depending on usage
4. *Rationale*: We chose this option because it is a free, flexible, cloud database and has seamless integration with our choice to use Firebase Cloud Functions to input data, and also Firebase hosting. Firestore is secure and can easily be used to retrieve individual documents (searching a specific book) or all documents based on specific queries (featured page or similar books based on keywords). Firestore also can be used with Firebase authentication and we can store user data as well.