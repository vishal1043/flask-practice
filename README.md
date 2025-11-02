# Flask + MySQL Todo App

A simple **Task Management Web Application** built with **Flask** and **MySQL**, using **SQLAlchemy ORM** for database operations.
This project lets users **add, update, view, and delete** todo items — serving as a foundation for larger task management or analytics systems.

---

## Features

* Add new tasks with title and description
* View all tasks on the main page
* Update existing tasks
* Delete tasks
* Uses SQLAlchemy ORM for database management
* MySQL backend for persistent storage

---

## Tech Stack

* **Backend:** Flask (Python)
* **Database:** MySQL (via `mysql-connector` and SQLAlchemy)
* **Templating:** Jinja2 / HTML
* **Frontend:** HTML, CSS (customizable)
* **ORM:** SQLAlchemy

---

## Setup & Installation

### 1. Clone the Repository

```bash
git clone https://github.com/<your-username>/flask-todo-app.git
cd flask-todo-app
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
venv\Scripts\activate    # On Windows
source venv/bin/activate # On macOS/Linux
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

If you don’t have a `requirements.txt` yet, create one with:

```bash
pip freeze > requirements.txt
```

### 4. Configure Database

* Make sure you have **MySQL** installed and running.
* Create a database (for example: `todo`):

  ```sql
  CREATE DATABASE todo;
  ```
* Update your MySQL username, password, and database name in the app configuration:

  ```python
  app.config['SQLALCHEMY_DATABASE_URI'] = 'mysql+mysqlconnector://<user>:<password>@localhost/<database_name>'
  ```

---

## Run the Application

Run the following command inside your project directory:

```bash
python app.py
```

Then open your browser and visit:

```
http://127.0.0.1:8000/
```

---

## Project Structure

```
├── app.py
├── templates/
│   ├── index.html
│   └── update.html
├── static/          # (optional: CSS, JS, images)
├── requirements.txt
└── README.md
```

---

##  CRUD Functionality Overview

| Route           | Method    | Description                             |
| --------------- | --------- | --------------------------------------- |
| `/`             | GET, POST | View all tasks / Add new task           |
| `/update/<sno>` | GET, POST | Edit existing task                      |
| `/delete/<sno>` | GET, POST | Delete a task                           |
| `/show`         | GET       | Test route (shows all tasks in console) |

---

## Future Enhancements

* Add user authentication (Flask-Login)
* Integrate analytics dashboard (Chart.js)
* Add task completion tracking
* Deploy on Render / Heroku

---

