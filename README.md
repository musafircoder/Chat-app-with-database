# Chat-app-with-database
A simple chat application with a PostgreSQL backend. Supports real-time messaging, user management, and persistent storage for conversations.
Perfect, thanks for sharing the code. I see it’s a **FastAPI-based chat app** with:

* **WebSocket** support for real-time messaging
* A very simple **HTML/JS frontend**
* **PostgreSQL database integration** (through SQLAlchemy) to save messages
* Broadcast + personal messages through a connection manager

No sensitive information is exposed in this file (looks clean — credentials probably live in `database.py`, which you’ll want to keep private or config-driven).

Here’s the **GitHub description** and a full **README.md** tailored to your code:

---

### GitHub Description

A FastAPI chat application with PostgreSQL persistence. Features include WebSocket-based real-time messaging, a simple frontend, and message storage with SQLAlchemy.

---

### README.md

# FastAPI Chat App with PostgreSQL

This project is a chat application built with **FastAPI** that supports real-time messaging over WebSockets. Messages are stored in a **PostgreSQL database** using SQLAlchemy. It comes with a simple HTML/JavaScript frontend for testing.

## Features

* Real-time chat with WebSockets
* PostgreSQL integration for message persistence
* Broadcasts join, leave, and chat messages to all connected clients
* Minimal HTML/JavaScript frontend included for quick testing

## Tech Stack

* **Backend:** FastAPI
* **Database:** PostgreSQL
* **ORM:** SQLAlchemy
* **Frontend:** Plain HTML + JavaScript

## Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/your-username/fastapi-chat-app.git
cd fastapi-chat-app
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure the database

Edit your `database.py` file to include the PostgreSQL connection string. Example:

```python
DATABASE_URL = "postgresql+psycopg2://username:password@localhost:5432/chat_db"
```

*(Do not hardcode credentials into GitHub. Use environment variables or a `.env` file and add it to `.gitignore`.)*

### 4. Run the application

```bash
uvicorn main:app --reload
```

### 5. Open in browser

Visit: [http://localhost:8000](http://localhost:8000)

Each new client is assigned a random ID. Messages are broadcast to all connected users and stored in the database.
