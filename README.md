# Task Manager

A simple task management application built using **Node.js**, **Express**, **SQLite**, and **Tailwind CSS** for managing tasks with priorities and descriptions.

## Features

- Add tasks with:
  - **Title**
  - **Description**
  - **Priority**: High, Medium, or Low
- Display tasks with:
  - Title and description
  - Priority shown below the title
- Sort tasks automatically based on priority (`High` > `Medium` > `Low`).
- Mark tasks as complete or undo the completion.
- Delete tasks.
- Responsive and visually appealing design using Tailwind CSS.

## Prerequisites

Ensure you have the following installed:

- **Node.js** (v14 or later)
- **npm** (comes with Node.js)
- **SQLite3**

## Installation

1. Clone this repository:

```bash
   git clone https://github.com/yourusername/task-manager.git
   cd task-manager
```

2. Install dependencies:

```bash
   npm install
```

3. Start the server:

```bash
   node server.js
```

4. Open your browser and navigate to:

```bash
   http://localhost:3000
```

## Project Structure

```sh
task-manager/
├── server.js          # Main backend server
├── database.db        # SQLite database file (auto-generated)
├── public/            # Static files served to the client
│   ├── index.html     # Frontend HTML file
│   ├── script.js      # Frontend JavaScript for functionality
│   └── style.css      # Tailwind CSS linked
├── package.json       # Node.js configuration file
└── README.md          # Project documentation
```

## API Endpoints

### `GET /tasks`

- Fetches all tasks from the database.
- Tasks are sorted by priority (`high`, `medium`, `low`) and by creation order within the same priority.

### `POST /tasks`

- Creates a new task.
- **Request Body** (JSON):

```json
  {
    "text": "Task title",
    "description": "Task description",
    "priority": "high"
  }
```

### `PUT /tasks/:id`

- Updates a task's completion status.
- **Request Body** (JSON):

```json
  {
    "completed": true
  }
```

### `DELETE /tasks/:id`

- Deletes a task by ID.

## Usage

1. **Add a New Task**:
   - Enter the task title, description, and select its priority.
   - Click "Add" to save the task.

2. **View Tasks**:
   - Tasks are displayed with their titles, descriptions, and priorities.
   - Tasks are automatically sorted by priority.

3. **Mark as Complete**:
   - Click the "Complete" button to mark a task as completed.
   - Click "Undo" to unmark a completed task.

4. **Delete a Task**:
   - Click the "Delete" button to remove a task from the list.

## Screenshots

1. **Task Form**
   Allows users to add tasks with title, description, and priority.

2. **Task List**
   Displays tasks with their descriptions, priorities, and action buttons for completing or deleting tasks.

## Contributing

If you'd like to contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a pull request.
