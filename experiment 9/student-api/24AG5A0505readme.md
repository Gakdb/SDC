# 📘 Express.js CRUD Web Application with REST API for Student Data

This document explains how to develop an Express.js web application that performs CRUD operations on student data using RESTful APIs, and how to test it using Postman.

---

## 🏗️ OVERVIEW

You're building:
- A **backend server** using **Node.js + Express.js**
- A **RESTful API** to handle **CRUD operations** for student data
- You will **test API endpoints** using **Postman**

---

## 📦 TECHNOLOGY STACK

- **Node.js**: JavaScript runtime
- **Express.js**: Web framework for building APIs
- **MongoDB** *(optional)* or **local array/object** for storing student data
- **Postman**: API testing tool

---

## 🧱 STEP-BY-STEP STRUCTURE

### 1️⃣ Set Up the Project

**Initial setup:**
- Create a new folder for the project.
- Initialize it with `npm init`.
- Install Express: `npm install express`
- Optional: Install body-parser, nodemon (for live server reload)

**File structure:**
```
student-crud-api/
│
├── server.js              # Main entry point
├── routes/
│   └── studentRoutes.js   # All student-related routes
├── controllers/
│   └── studentController.js # Functions that handle request logic
├── models/
│   └── student.js         # (Optional) Schema for MongoDB
├── package.json
```

---

### 2️⃣ Create REST API Endpoints

Your **REST API** should follow these conventions:

| Operation       | HTTP Method | Endpoint            | Description                  |
|----------------|-------------|---------------------|------------------------------|
| Create Student  | `POST`      | `/students`         | Add a new student            |
| Read All        | `GET`       | `/students`         | Get all students             |
| Read by ID      | `GET`       | `/students/:id`     | Get one student by ID        |
| Update Student  | `PUT`       | `/students/:id`     | Update student details       |
| Delete Student  | `DELETE`    | `/students/:id`     | Remove student by ID         |

**How it works:**
- Express listens for incoming requests on these routes.
- A controller function processes the request and returns a response.

---

### 3️⃣ Using a Database (Optional)

If using MongoDB:
- Use Mongoose to define a schema for the `Student` model.
- Connect to a local or cloud MongoDB database.
- Store student records in a collection.

If not:
- Use a temporary array or object to mimic database behavior in memory.

---

### 4️⃣ Use Postman for API Testing

🔧 **Postman** lets you simulate client requests:

#### ➕ POST `/students`
- Go to Postman > Select `POST`
- URL: `http://localhost:3000/students`
- Body tab → raw → JSON
```json
{
  "name": "Alice",
  "age": 21,
  "course": "Computer Science"
}
```

#### 📥 GET `/students`
- Select `GET`
- URL: `http://localhost:3000/students`
- Click **Send** → You’ll see all student records

#### 🧾 GET `/students/:id`
- Replace `:id` with the actual student ID
- Returns a single student

#### 🔄 PUT `/students/:id`
- Use `PUT` with updated JSON in the body
```json
{
  "name": "Alice Johnson",
  "age": 22
}
```

#### ❌ DELETE `/students/:id`
- Sends a `DELETE` request to remove a student by ID

---

## 🔐 Additional Notes

- Use `express.json()` to parse JSON bodies
- Use `res.status().json()` to return meaningful responses
- Implement error handling (e.g., student not found, invalid input)
- You can use UUID or MongoDB `_id` for unique student identifiers

---

## ✅ Summary

You’ve built:
- A **Node.js + Express app**
- That exposes **RESTful API routes**
- Connected to an optional database (or in-memory structure)
- Tested via **Postman** to **Create, Read, Update, Delete** student data

---

## 🧠 Next Steps

- Add user authentication (e.g., JWT)
- Integrate with a frontend (React, Angular)
- Deploy to cloud platforms (Render, Railway, Vercel)
