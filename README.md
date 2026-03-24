# Permalist 📝

A persistent To-Do List web app where your tasks actually survive a server restart — because what's the point of a to-do list that forgets everything?

## Tech Stack

- **Backend** — Node.js + Express
- **Templating** — EJS
- **Database** — PostgreSQL
- **Styling** — CSS

## Features

- Add new tasks
- Delete tasks
- Edit existing tasks
- Data persists via PostgreSQL (no more in-memory arrays that vanish on restart)

## Prerequisites

- [Node.js](https://nodejs.org/) v18+
- [PostgreSQL](https://www.postgresql.org/) running locally or via a cloud provider

## Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/AnushiBisht/Permalist.git
cd Permalist
```

### 2. Install dependencies

```bash
npm install
```

### 3. Set up the database

Create a PostgreSQL database and run the following to set up the table:

```sql
CREATE TABLE items (
  id SERIAL PRIMARY KEY,
  title VARCHAR(100) NOT NULL
);
```

### 4. Configure environment variables

Create a `.env` file in the root directory:

```env
DB_USER=your_pg_username
DB_HOST=localhost
DB_NAME=your_database_name
DB_PASSWORD=your_pg_password
DB_PORT=5432
```

### 5. Run the app

```bash
npm start
```

App will be running at `http://localhost:3000`

## Project Structure

```
Permalist/
├── public/          # Static assets (CSS)
├── views/           # EJS templates
├── index.js         # Main server file
├── .env             # Environment variables (not committed)
└── package.json
```

## License

ISC
