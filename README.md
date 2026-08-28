# Project Manager App

A React app for tracking projects and todos, with a project list and a todo list pulled from a live API.

## Features

- Add a project with a title and category (Web Design, Web Development, Mobile Development, etc.)
- Delete any project from the list
- Displays a todo list fetched live from JSONPlaceholder's free testing API

## Tech Stack

- React 16.3.2 (Create React App / react-scripts 1.1.4)
- [JSONPlaceholder](https://jsonplaceholder.typicode.com/) API (free, no key required) for the todo list

## Getting Started

This project uses an older version of `react-scripts` that requires Node 16 (newer Node versions will throw an OpenSSL-related build error).

```bash
git clone https://github.com/tnelson2016/Project-Manager-App-built-in-React.git
cd Project-Manager-App-built-in-React
nvm use 16          # or use NODE_OPTIONS=--openssl-legacy-provider on newer Node
npm install --omit=optional
npm start
```

The app will open at [http://localhost:3000](http://localhost:3000).

## Known Issues

- No styling — functional but plain, uses default browser form/list rendering
- Projects are stored in local component state only (not persisted, resets on refresh)
- Todo list content is placeholder/test data from JSONPlaceholder, not meaningful task data
- No test coverage beyond the default CRA smoke test

## Project Structure

```
src/
  Components/
    AddProject.js       # New-project form (title + category)
    Projects.js          # Renders the list of projects
    ProjectItem.js        # Single project row with delete link
    Todos.js               # Fetches and renders the todo list
    TodoItem.js              # Single todo row
  App.js                     # Root component, holds project state
```