
# Travel Tracker

This is a simple web application that allows you to track countries you have visited. It uses Node.js with Express, EJS for templating, and PostgreSQL as the database.

---

## Features

- Display a list of countries you have visited.
- Show the total number of countries visited.

---

## Technologies Used

- **Node.js**: JavaScript runtime environment.
- **Express.js**: Fast, unopinionated, minimalist web framework for Node.js.
- **EJS (Embedded JavaScript)**: Simple templating language that lets you generate HTML with plain JavaScript.
- **PostgreSQL**: Powerful, open-source object-relational database system.
- **pg**: Non-blocking PostgreSQL client for Node.js.
- **body-parser**: Node.js body parsing middleware.

---

## Setup and Installation

To get this project up and running on your local machine, follow these steps:

### 1. Prerequisites

Make sure you have the following installed:

- Node.js (LTS version recommended)
- PostgreSQL

### 2. Database Setup

First, set up your PostgreSQL database.

#### Create a database:

```sql
CREATE DATABASE world;
````

#### Create a table named `visited_countries` in your `world` database:

```sql
CREATE TABLE visited_countries (
    id SERIAL PRIMARY KEY,
    country_code VARCHAR(2) NOT NULL UNIQUE
);
```

#### Update Database Credentials

Open `index.js` and update the database connection details with your PostgreSQL credentials:

```js
const db = new pg.Client({
  user: "postgres", // Your PostgreSQL username
  host: "localhost",
  database: "world",
  password: "3023Qw#Myung", // Your PostgreSQL password
  port: 5432,
});
```

### 3. Project Setup

Clone the repository (if you haven't already):

```bash
git clone <your-repository-url>
cd 8.3-travel-tracker
```

Install dependencies:

```bash
npm install
```

### 4. Running the Application

Start the server:

```bash
node index.js
```

Access the application:

Open your web browser and go to: [http://localhost:3000](http://localhost:3000)

---

## Project Structure

* `index.js`: The main server file, handling routes and database interactions.
* `views/`: Contains EJS template files (e.g., `index.ejs`).
* `public/`: Static assets like CSS files.
* `package.json`: Lists project dependencies and scripts.

---

## Usage

Once the application is running, you will see a list of countries you have visited (initially empty if your database table is new). You can extend this application to add functionality for adding new countries, deleting, or updating.

---

