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

creat_router.js

2. What do you notice about the folder structure?  Whats the client responsible for? Whats the server responsible for?

The client is reponsible for the user interface and input of the app. The vue files are responsible for what the user sees (HTML and CSS) and how they can interact with the site itself. The server is seeding the initial data and stores the routes for the app. It has preloaded the various CRUD options for the user. When the user inputs information, the client side takes that information, passes it through the appropriate methods and then the server side uses that information to update the app.

3. What are the the responsibilities of server.js?

Server.js is creating the link to the database and the localhost, as well as setting up the various db's.

4. What are the responsibilities of the `gamesRouter`?

The gamesRouter is giving access to the REST routes for the app.

5. What process does the the client (front-end) use to communicate with the server?

The URL they input?

6. What optional second argument does the `fetch` method take? And what is it used for in this application? Hint: See [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) on the MDN docs

It is taking an optional init object and in this application we are inserting a method (POST and DELETE)

7. Which of the games API routes does the front-end application consume (i.e. make requests to)?

router.get?

8. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?

The driver is used to convert various datatypes to the BSON that mongo stores.


## Extension

Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?

Add to your diagram the dataflow for removing a game.
