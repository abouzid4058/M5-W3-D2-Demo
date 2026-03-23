# m5-w3-d2-exercise: CRUD with JSON Server

## Module 5 - Week 3 - Day 2: RESTful API CRUD with React + JSON Server

This React app demonstrates **GET (Read)** from a RESTful API using `json-server` as a local mock database.

---

## What It Does

- Runs a local JSON Server on port 5000 serving `db.json` as a REST API
- React app fetches the list of books from `http://localhost:5000/posts`
- Clicking **"Get Lists"** loads and displays all books in a Bootstrap-styled table
- Uses `concurrently` to run both the React app and JSON Server at the same time

---

## Project Structure

```
crud-json-server/
├── db.json              ← JSON database (books data)
├── package.json         ← Scripts + dependencies
├── public/
│   └── index.html
└── src/
    ├── index.js         ← React entry point
    ├── App.js           ← Parent component (GET handler, state, render)
    └── Lists.js         ← Child component (renders data table)
```

---

## Setup & Run

```bash
# Install dependencies
npm install

# Run React app + JSON Server concurrently
npm run dev
```

Visit [http://localhost:3000](http://localhost:3000) and click **Get Lists**.

The JSON Server runs at [http://localhost:5000/posts](http://localhost:5000/posts).

---

## Key Concepts

- **json-server** — Turns `db.json` into a full REST API (GET, POST, PUT, DELETE)
- **concurrently** — Runs multiple npm scripts simultaneously
- **Fetch API** — Used to GET data from the JSON Server
- **React class component** — `App.js` uses class-based state and event handlers
- **Props** — `App.js` passes fetched data down to `Lists.js` via `alldata` prop
