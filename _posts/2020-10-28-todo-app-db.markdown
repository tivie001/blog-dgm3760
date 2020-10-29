---
layout: post
title:  "Blog Post #8 - Todo App Backend"
---
![Todo App Screenshot](/assets/todo-app.png)

## Todo App Assignment (w/ MongoDB & ExpressJS)
### [Todo App URL](https://todo-app-dgm3760.herokuapp.com/)

--------------------------------------------------------------------------------

#### How did you design/architect your app and server?

This app implements a frontend with HTML, CSS, and JS. From the main.js
file the user may interact with the app which then send requests to
and from the server (using the Fetch API) built with ExpressJS in Node. The following endpoints
use mongoose model schema methods to create, update, delete, and get todos.

#### Why did you choose the design you did?

* I decided to use vanilla HTML, CSS, & JS because I had most of it implemented
from last project and it made most sense to continue to use that functionality.

* I went with MongoDB for the database because it was easy, a lot of documentation
backing it, and I wanted to learn more about NoSQL databases.

#### How did you model your data and why?

The two models used are: 

1. Todo Model 
2. Category Model

Both models are relational by category so, the todos and categories can be
correlated and be easily filtered by a category.

#### Why is documentation important?

Because it helps you first off, know how your app is working and makes for good 
structured code. Second off, it helps developers know, understand, and use your 
code after you. 