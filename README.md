# Spendly

A personal expense tracker built with Flask — a learning project to practice
Python web development, SQLite, and basic auth flows.

> Track every rupee. Own your finances.

## Status

Work in progress. Being built incrementally, step by step:

- [x] Landing, register, and login pages (templates + routes)
- [ ] Database layer (`database/db.py`) — `get_db()`, `init_db()`, `seed_db()`
- [ ] Logout
- [ ] Profile page
- [ ] Add expense
- [ ] Edit expense
- [ ] Delete expense

Routes not yet implemented currently return a placeholder string instead of
a real page.

## Tech stack

- [Flask](https://flask.palletsprojects.com/) 3.1 — web framework
- SQLite — storage (via `database/db.py`)
- Jinja2 templates + vanilla CSS/JS (no frontend framework)
- [pytest](https://docs.pytest.org/) + [pytest-flask](https://pytest-flask.readthedocs.io/) — testing

## Project structure

```
app.py                  Flask app and routes
database/
  db.py                 SQLite connection, schema, seed data
static/
  css/style.css
  js/main.js
templates/
  base.html              Shared layout (nav, footer)
  landing.html
  register.html
  login.html
requirements.txt
```

## Setup

Create a virtual environment and install dependencies:

```powershell
python -m venv nvenv
nvenv\Scripts\Activate.ps1
pip install -r requirements.txt
```

## Running the app

```powershell
nvenv\Scripts\python.exe app.py
```

The app runs in debug mode at **http://127.0.0.1:5001**.

## Running tests

```powershell
nvenv\Scripts\python.exe -m pytest
```
