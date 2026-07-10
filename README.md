# Phonebook API

A REST API for a contacts/phonebook application, built with Node.js, Express, and MongoDB (via Mongoose). Handles storing, retrieving, updating, and deleting contacts, and serves the built frontend in production.

🔗 **Live app:** [full-stack-open-part3-u6p2.onrender.com](https://full-stack-open-part3-u6p2.onrender.com/)

## About this project

Originally built as part of the Full Stack Open course (University of Helsinki), this repo covers the backend I implemented: a REST API with a MongoDB database, environment-based configuration, and a production deployment on Render, serving a phonebook frontend.

## Features

- Full CRUD REST API for contacts (create, read, update, delete)
- MongoDB persistence via Mongoose schemas/models
- Environment-based configuration (`.env` for DB connection string, port)
- Centralized error handling and request logging middleware
- Serves the compiled frontend build in production, so the API and UI run from a single deployed service

## Tech stack

| Technology | Purpose |
|---|---|
| Node.js | Runtime |
| Express | Web server / routing |
| MongoDB | Database |
| Mongoose | ODM / schema modeling |
| dotenv | Environment variable management |
| Render | Deployment |

## API endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/persons` | Get all contacts |
| GET | `/api/persons/:id` | Get a single contact |
| POST | `/api/persons` | Add a new contact |
| DELETE | `/api/persons/:id` | Delete a contact |

## Project structure

```
├── dist/            # compiled production files
├── uibuild/          # production frontend build (served by Express)
├── models/          # Mongoose model definitions
├── requests/        # sample REST API requests for manual testing
├── index.js         # Express server entry point
├── mongo.js         # standalone script for interacting with MongoDB
└── eslint.config.mjs
```

## Running locally

```bash
git clone https://github.com/DenisHki/phonebook-api.git
cd phonebook-api
npm install
```

Create a `.env` file:

```
MONGODB_URI=your_mongodb_connection_string
PORT=3001
```

Start the server:

```bash
npm start
```

The server runs at [http://localhost:3001](http://localhost:3001).

## Background

This project was built while completing the [Full Stack Open](https://fullstackopen.com/) course by the University of Helsinki, which covers modern web development with React, Node.js, and MongoDB. This repo represents the backend/deployment portion of that work.
