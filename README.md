# Student API with Gin

A simple REST API built with Gin and SQLite using layered architecture.

---

## 📦 Project Structure

go-api-gin/
├─ main.go
├─ models/
├─ repositories/
├─ services/
├─ handlers/
├─ config/
└─ students.db

---

## 🚀 How to Run

 
1. Install dependencies
```bash
go mod tidy

2. Run the server
go run main.go

Server will start at: http://localhost:8080


### Available API Endpoints

🔹 Get All Students
GET /students

🔹 Get Student by ID
GET /students/:id

🔹 Create Student
POST /students

Body (JSON):

{
  "id": "6609650509",
  "name": "Phachara Pornpong",
  "major": "Computer Science",
  "gpa": 4
}

🔹 Update Student
PUT /students/:id

Body (JSON):

{
  "name": "Hammy Hamster",
  "major": "Computer Science",
  "gpa": 3.5
}

Returns 404 if student not found.

🔹 Delete Student
DELETE /students/:id

Returns:

- 204 No Content (success)

- 404 Not Found


✅ Validation Rules :

- id must not be empty

- name must not be empty

- gpa must be between 0.00 and 4.00


Phachara Pornpong 6609650509