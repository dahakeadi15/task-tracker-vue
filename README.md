# Tasks Tracker

A simple Tasks Tracker application built with Vue.js, where you can add, delete, and toggle the reminder state of tasks. This app uses `json-server` to simulate a backend API, providing a database to store and retrieve tasks.

## Features

- Add new tasks using a form.
- Toggle the visibility of the task form with the "Add Task" button.
- Display a list of tasks with text and date.
- Mark tasks as "remind" by double-clicking on them, which highlights the item.
- Delete tasks.
- Persistent data storage with a mock REST API using `json-server`.

## Demo

You can see the live demo of this project by running it locally, as detailed in the "Setup" section.

## Setup

### Prerequisites

Ensure you have the following installed on your machine:

- Node.js (https://nodejs.org/)
- npm (comes bundled with Node.js)

### Getting Started

1. Clone the repository:

   ```bash
   git clone https://github.com/dahakeadi15/task-tracker-vue.git
   cd tasks-tracker-vue
   ```

2. Install project dependencies:

   ```bash
   npm install
   ```

3. Install `json-server` as a development dependency:

   ```bash
   npm install json-server --save-dev
   ```

4. Set up the mock database:
   You can configure the `json-server` to run by creating a `db.json` file (if not already present). Here’s a simple example of the content of the file:

   ```json
   {
     "tasks": []
   }
   ```

5. Start the Vue.js development server and the json-server API:

   ```bash
   npm run serve
   ```

   ```bash
   npm run api
   ```

   The Vue app should now be running at `http://localhost:8080`, and the mock API is available at `http://localhost:5000/tasks`.

### Project Structure

- `src/` - The main source code for the Vue app.
  - `components/` - Contains Vue components such as the Task list, Task item, and the Add-task form.
  - `assets/` - Static assets such as images or icons.
  - `App.vue` - The root component.
  - `main.js` - The entry point for Vue, where the app is mounted.
- `public/` - The public folder for static files.
- `db.json` - The mock database used by `json-server` to persist tasks.
- `package.json` - Contains project dependencies and scripts.

### Scripts

- `npm run serve`: Starts the Vue.js development server at `http://localhost:8080`.
- `npm run api`: Starts `json-server` to serve the mock API at `http://localhost:5000`.
- `npm run build`: Builds the app for production, optimizing files for deployment.

## Usage

1. Open the app in your browser at `http://localhost:8080`.
2. Click the "Add Task" button to toggle the form and add a new task.
3. The task list will display each item with:
   - The task text.
   - The date of the task.
   - A delete button to remove the item.
   - Double-clicking a task will toggle the reminder state, which highlights the task item.
4. Data is persisted across page reloads via `json-server`.
