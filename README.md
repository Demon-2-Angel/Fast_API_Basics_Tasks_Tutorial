# Task Manager REST API (FastAPI)

A simple **RESTful Task Management API** built using **FastAPI**.  
This project demonstrates clean REST principles, proper HTTP semantics, request/response validation, and error handling.

---

## 🚀 Features

- Create, read, update, and delete tasks (CRUD)
- Proper RESTful endpoint design
- UUID-based task identification
- Input validation using Pydantic
- Correct HTTP status codes
- Auto-generated API documentation (Swagger)

---

## 🧠 REST Design Principles Followed

- **Resources, not actions** (`/tasks`, `/tasks/{id}`)
- Correct HTTP methods (`GET`, `POST`, `PUT`, `DELETE`)
- Stateless requests
- Clear request & response models
- Meaningful error responses (`404 Not Found`)

---

## 📦 Tech Stack

- **Python 3.11**
- **FastAPI**
- **Uvicorn**
- **Pydantic**

---

## 📁 Project Structure

# Task Manager REST API (FastAPI)

---

## 📁 Project Structure
```
├── main.py
└── README.md
```

---

## ▶️ How to Run the Project

### 1️⃣ Install dependencies
```bash
pip install fastapi uvicorn
```
2️⃣ Start the server (recommended)
```
uvicorn main:app --reload
```

3️⃣ Open in browser

API Base URL
```
http://localhost:8000
```
Swagger Docs
```
http://localhost:8000/docs
```
🧩 API Endpoints
➕ Create Task
```
POST /tasks/
```
Request Body
```
{
  "title": "Learn FastAPI",
  "description": "Build a REST API",
  "completed": false
}
```
Response

```
{
  "id": "uuid",
  "title": "Learn FastAPI",
  "description": "Build a REST API",
  "completed": false
}
```

📄 Get All Tasks
GET /tasks/

Response
```
[
  {
    "id": "uuid",
    "title": "Learn FastAPI",
    "description": "Build a REST API",
    "completed": false
  }
]
```
🔍 Get Task by ID
GET /tasks/{task_id}

Returns 404 if task does not exist

✏️ Update Task
PUT /tasks/{task_id}

Request Body
```
{
  "title": "Learn REST",
  "completed": true
}
```
Updates only provided fields

Returns 404 if task does not exist

❌ Delete Task
DELETE /tasks/{task_id}

Response
```
{
  "id": "uuid",
  "title": "Learn REST",
  "description": "Build a REST API",
  "completed": true
}
```
⚠️ Error Handling
Example 404 Response
```
{
  "detail": "Task not found"
}
```
📌 Important Notes
Data is stored in-memory (list), not persisted

Restarting the server clears all tasks

Designed for learning REST API fundamentals

🔮 Future Improvements
Separate request and response schemas

- Add PATCH endpoint
- Add pagination and filtering
- Add authentication (JWT)

Persist data using a database (SQLite/PostgreSQL)

🧪 Why This Project Matters
This project demonstrates:
  
  1. Correct REST API design
  
  2. Backend engineering fundamentals
  
  3. Clean FastAPI usage
  
  4. Interview-ready API implementation

👤 Author
Aniruddha Kumar


📝 License
This project is for learning and educational purposes.

---

### ChatGPT Opinion
This README is **clean, readable, and GitHub-ready**.  
It explains *what the project does* without overengineering or unnecessary theory.

Next time you add:
- PATCH
- DB
- Auth

You can just extend this README instead of rewriting it.

If you want, next I can:
- Make this **resume-ready project description**
- Add **curl examples**
- Prepare **interview explanation bullets** for this API
