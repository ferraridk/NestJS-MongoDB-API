### NestJS MongoDB API

<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="120" alt="Nest Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

  <p align="center">A progressive <a href="http://nodejs.org" target="_blank">Node.js</a> framework for building efficient and scalable server-side applications.</p>
    <p align="center">
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/v/@nestjs/core.svg" alt="NPM Version" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/l/@nestjs/core.svg" alt="Package License" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/dm/@nestjs/common.svg" alt="NPM Downloads" /></a>
<a href="https://circleci.com/gh/nestjs/nest" target="_blank"><img src="https://img.shields.io/circleci/build/github/nestjs/nest/master" alt="CircleCI" /></a>
<a href="https://coveralls.io/github/nestjs/nest?branch=master" target="_blank"><img src="https://coveralls.io/repos/github/nestjs/nest/badge.svg?branch=master#9" alt="Coverage" /></a>
<a href="https://discord.gg/G7Qnnhy" target="_blank"><img src="https://img.shields.io/badge/discord-online-brightgreen.svg" alt="Discord"/></a>
<a href="https://opencollective.com/nest#backer" target="_blank"><img src="https://opencollective.com/nest/backers/badge.svg" alt="Backers on Open Collective" /></a>
<a href="https://opencollective.com/nest#sponsor" target="_blank"><img src="https://opencollective.com/nest/sponsors/badge.svg" alt="Sponsors on Open Collective" /></a>
  <a href="https://paypal.me/kamilmysliwiec" target="_blank"><img src="https://img.shields.io/badge/Donate-PayPal-ff3f59.svg" alt="Donate us"/></a>
    <a href="https://opencollective.com/nest#sponsor"  target="_blank"><img src="https://img.shields.io/badge/Support%20us-Open%20Collective-41B883.svg" alt="Support us"></a>
  <a href="https://twitter.com/nestframework" target="_blank"><img src="https://img.shields.io/twitter/follow/nestframework.svg?style=social&label=Follow" alt="Follow us on Twitter"></a>
</p>
  <!--[![Backers on Open Collective](https://opencollective.com/nest/backers/badge.svg)](https://opencollective.com/nest#backer)
  [![Sponsors on Open Collective](https://opencollective.com/nest/sponsors/badge.svg)](https://opencollective.com/nest#sponsor)-->

## Description
This project is a backend application built with NestJS, providing a RESTful API that connects to a MongoDB database. The application includes functionality for managing users and posts using Mongoose as the Object Data Modeling (ODM) library.

## Features
CRUD operations for users and posts.
MongoDB integration with Mongoose.
Data validation using ValidationPipe.
Centralized management of environment variables using dotenv and @nestjs/config.
Installation
Follow these steps to install and run the project locally.

## Prerequisites
* Node.js (version 16 or newer)
* MongoDB (You can use a local MongoDB instance or MongoDB Atlas)
* npm (Node Package Manager)

# Step 1: Clone the repository
Clone the repository to your local machine:

```bash
git clone https://github.com/your-github-username/nestjs-mongodb.git
```

# Step 2: Install dependencies
Navigate to the project directory and install the required dependencies:

```bash
cd nestjs-mongodb
npm install
```

# Step 3: Create a .env file
Create a .env file in the root of the project with the following content:

env:
MONGODB_URI=your-mongodb-connection-string
PORT=3000  # Or any port you prefer

Replace your-mongodb-connection-string with your actual MongoDB connection string. If you're using MongoDB Atlas, the URI will look something like this:

bash
mongodb+srv://<username>:<password>@cluster0.mongodb.net/<dbname>?retryWrites=true&w=majority

# Step 4: Start the application
Now you can start the application with the following command:

```bash
npm run start
```
The application will be running on http://localhost:3000.

# Step 5: API Documentation
You can use Postman or Insomnia to test the API endpoints. The default endpoints include:

## Users API:

GET /users - Retrieve all users
POST /users - Create a new user
GET /users/:id - Retrieve a user by ID
PATCH /users/:id - Update a user by ID
DELETE /users/:id - Delete a user by ID

## Posts API:

GET /posts - Retrieve all posts
POST /posts - Create a new post
GET /posts/:id - Retrieve a post by ID
PATCH /posts/:id - Update a post by ID
DELETE /posts/:id - Delete a post by ID

## Project Structure
Here is an overview of the project structure:

```bash
├── src
│   ├── app.module.ts        # Main module for the application
│   ├── main.ts              # Application entry point
│   ├── users
│   │   ├── users.controller.ts  # API routes for User resources
│   │   ├── users.module.ts      # Module for User functionality
│   │   ├── users.service.ts     # Business logic for Users
│   │   └── schemas
│   │       └── user.schema.ts   # Mongoose schema for User model
│   └── posts
│       ├── posts.controller.ts  # API routes for Post resources
│       ├── posts.module.ts      # Module for Post functionality
│       ├── posts.service.ts     # Business logic for Posts
│       └── schemas
│           └── post.schema.ts   # Mongoose schema for Post model
├── .env                       # Environment variables (ignored in version control)
├── package.json                # Project dependencies and scripts
├── tsconfig.json               # TypeScript configuration
└── README.md                   # Project documentation
```

## Technologies
This project uses the following technologies:

* NestJS - A progressive Node.js framework for building efficient and scalable server-side applications.
* Mongoose - ODM (Object Data Modeling) library for MongoDB.
* TypeScript - Strongly typed JavaScript.
* MongoDB - NoSQL database for data storage.

## Development Commands
Run the project in development mode:

```bash
npm run start:dev
Build the project:
```
```bash
npm run build
Run tests:
```
```bash
npm run test
```
## Contribution
Feel free to contribute by submitting a pull request or opening an issue in the GitHub repository.