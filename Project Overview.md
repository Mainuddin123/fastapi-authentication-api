# 🔐 FastAPI Authentication API

A secure Authentication API built using **FastAPI**, **PostgreSQL**, **SQLAlchemy**, **Pydantic**, and **Passlib (bcrypt)**. This project demonstrates user registration, secure password hashing, user login, and login history tracking with a clean modular architecture.

---

## 🚀 Features

- User Registration
- Secure Password Hashing (bcrypt)
- User Login Authentication
- Login History Tracking
- PostgreSQL Database Integration
- SQLAlchemy ORM
- Pydantic Data Validation
- FastAPI Swagger Documentation
- Modular Project Structure

---

## 🛠️ Tech Stack

- Python
- FastAPI
- PostgreSQL
- SQLAlchemy
- Pydantic
- Passlib (bcrypt)
- Uvicorn

---

## 📂 Project Structure

```text
auth_project/
│
├── database/
│   └── connection.py
│
├── models/
│   ├── user_model.py
│   └── login_log_model.py
│
├── routers/
│   └── auth_router.py
│
├── schemas/
│   ├── user_schema.py
│   └── login_schema.py
│
├── services/
│   └── auth_service.py
│
├── utils/
│   └── hash.py
│
├── main.py
├── requirements.txt
├── .gitignore
└── README.md
```

---

## ⚙️ Installation

### Clone Repository

```bash
git clone https://github.com/Mainuddin123/fastapi-authentication-api.git
```

```bash
cd fastapi-authentication-api
```

### Create Virtual Environment

```bash
python -m venv venv
```

### Activate Virtual Environment

**Windows**

```bash
venv\Scripts\activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🗄️ PostgreSQL Configuration

Create a PostgreSQL database:

```sql
CREATE DATABASE auth_db;
```

Update the database URL in `database/connection.py`:

```python
DATABASE_URL = "postgresql://postgres:YOUR_PASSWORD@localhost:5432/auth_db"
```

---
## Compatibility Note

This project has been tested with:

- passlib==1.7.4
- bcrypt==4.0.1

## ▶️ Run the Application

```bash
uvicorn main:app --reload
```

---

## 📖 Swagger Documentation

Open your browser:

```
http://127.0.0.1:8000/docs
```

---

# 📌 API Endpoints

## Register User

**POST**

```
/register
```

Request

```json
{
  "username": "Mainuddin",
  "email": "mainuddin@gmail.com",
  "password": "Main@123"
}
```

---

## Login

**POST**

```
/login
```

Request

```json
{
  "username": "Mainuddin",
  "password": "Main@123"
}
```

---

## Get All Users

**GET**

```
/users
```

---

## Get Login Logs

**GET**

```
/login-logs
```

---

## 📸 Output

### ✅ Register User

```
User registered successfully
```

### ✅ Login

```
Login successful
```

### ✅ Get Users

```
Returns all registered users.
```

### ✅ Login Logs

```
Returns user login history.
```

---

## 🔒 Password Security

Passwords are securely hashed using **Passlib** with **bcrypt** before being stored in the PostgreSQL database.

---

## 📌 Future Improvements

- JWT Authentication
- Refresh Tokens
- Email Verification
- Forgot Password
- Role-Based Access Control (RBAC)
- Docker Support
- Unit Testing
- CI/CD Integration

---

## 👨‍💻 Author

**Shaik Khaja Mainuddin**

- GitHub: https://github.com/Mainuddin123
- LinkedIn: https://www.linkedin.com/in/shaik-khajamainuddin/

---

## ⭐ If you found this project useful, consider giving it a Star on GitHub!
