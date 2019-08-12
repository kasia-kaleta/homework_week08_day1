# Homework: Full Stack Games Hub App

### Learning Objectives

- Understand the relationship between client, server and database
- Be able to navigate a codebase that you haven't written

## Brief

Your boss has asked to you look over the codebase of a full-stack JavaScript application. The front-end is written in JavaScript using Vue, the back-end uses an Express server and a MongoDB database. Your task is to make yourself familiar with the codebase.

The application includes a README.md with instructions on running the application.

![Overview of the tech stack and tooling with commands](images/tech_stack_with_commands.png)

*Overview of the tech stack and tooling with commands*

## MVP

### Task

Draw a diagram showing the dataflow through the application starting with a form submission, ending with the re-rendering of the page. This will involve a multi-direction data-flow with the client posting data to the server and the server sending data back to the client with the response. Detail the client, server and database in the diagram and include the names of the files involved in the process.

### Questions

1. What is responsible for defining the routes of the `games` resource?
  - gamesRouter

2. What do you notice about the folder structure?  Whats the client responsible for? Whats the server responsible for?
  - The server is responsible for the back-end of application: accessing database, servers, routers.
  - The client folder is in charge of the front-end of application: this is what client is seeing on their browser, the files in the client folder are in charge of handling any changes or submissions made by client.

3. What are the the responsibilities of server.js?
  - connects to database
  - configuring the server
  - listens to requests

4. What are the responsibilities of the `gamesRouter`?
  - To delegate the routing for all the games resource

5. What process does the client (front-end) use to communicate with the server?
  - Submitting the new game form

6. What optional second argument does the `fetch` method take? And what is it used for in this application? Hint: See [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) on the MDN docs
  - The fetch() method can optionally accept a second parameter, an init object that allows you to control a number of different settings. In games_app it takes request POST method.

7. Which of the games API routes does the front-end application consume (i.e. make requests to)?
  -

8. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?
  - It provides both callback-based and Promise-based interaction with MongoDB, allowing applications to take full advantage of the new features in ES6.

## Extension

Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?

Add to your diagram the dataflow for removing a game.
