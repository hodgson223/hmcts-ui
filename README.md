# Task Manager React App

This project is a simple React application for creating, viewing, and deleting tasks. It connects to an Express gateway API running on `http://localhost:5000`, which then forwards requests to the backend task service.

## Features

- Create a new task
- View existing tasks
- Delete a task
- Display confirmation messages after actions
- Connect to a backend API using Axios

## Project Structure

```text
src/
├── App.js
├── TaskForm.js
├── index.js
└── index.css
```

## Main Components

### `App.js`
Renders the main layout and loads the `TaskForm` component.

### `TaskForm.js`
Handles:
- form input state
- fetching tasks from the backend
- submitting new tasks
- deleting tasks
- showing confirmation messages

### `index.js`
Entry point for the React application. It renders the `App` component inside the root element.

## Requirements

Before starting the React app, make sure you have:

- Node.js installed
- npm installed
- the Express API running on `http://localhost:5000`
- the backend task service running behind the API

## Installation

Install project dependencies:

```bash
npm install
```

## Running the Application

To start the React app, run:

```bash
npm start
```

The application should open in your browser at:

```text
http://localhost:3000
```

## How It Works

When the app loads:

1. `TaskForm` sends a `GET` request to `http://localhost:5000/tasks`
2. Existing tasks are displayed on the page

When a user submits the form:

1. A `POST` request is sent to `http://localhost:5000/tasks`
2. The form is reset
3. The task list refreshes

When a user deletes a task:

1. A `DELETE` request is sent to `http://localhost:5000/tasks/:id`
2. The deleted task is removed from the page

## Example Task Fields

Each task contains:

- `title`
- `description`
- `status`
- `dueDate`

## Notes

- The React frontend uses Axios for API requests
- The default task status is `Pending`
- Make sure the backend is running before using the form

## Author

Developed as part of a project using React, Axios, and a backend task API.

