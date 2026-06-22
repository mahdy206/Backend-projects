# 🎓 Student Management System

A secure, production-ready REST API built with **FastAPI** for managing university students, featuring JWT authentication, role-based access control, Redis caching, structured logging, a monitoring dashboard, a full frontend UI, and Docker support.

---

## ✨ Features

- 🔐 **JWT Authentication** — Register, login, and secure token-based access
- 👥 **Role-Based Authorization** — Admin vs Student permissions
- 📋 **Full CRUD** — Create, read, update, delete students
- 🔍 **Advanced Filtering** — Filter by department and minimum GPA
- 📄 **Pagination** — Configurable page size and number
- ⚡ **Redis Caching** — Cache-Aside pattern with automatic invalidation
- 📝 **Structured Logging** — File + terminal logs via Loguru
- 📊 **Monitoring Dashboard** — Live request/error metrics at `/monitoring/dashboard`
- 🧪 **API Testing** — Comprehensive pytest test suite with 20+ test cases
- 🎨 **Frontend UI** — Full HTML/CSS/JS interface for all CRUD operations
- 🐳 **Docker Support** — One-command startup with Docker Compose

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | FastAPI |
| Database | SQLite (Docker/dev) / SQL Server (local) |
| ORM | SQLAlchemy |
| Auth | JWT (python-jose) + bcrypt |
| Caching | Redis |
| Logging | Loguru |
| Testing | pytest + httpx |
| Frontend | HTML / CSS / JavaScript |
| Container | Docker + Docker Compose |

---

## 📁 Project Structure

```
student-management-system/
├── App/
│   ├── Auth/
│   │   ├── Jwt.py
│   │   └── Password.py
│   ├── Models/
│   ├── Schemas/
│   ├── Routes/
│   │   ├── Auth.py
│   │   ├── Students.py
│   │   └── Monitoring.py
│   ├── Services/
│   ├── Utils/
│   ├── Database.py
│   └── Main.py
├── Tests/
├── frontend/
│   └── index.html
├── Dockerfile
├── docker-compose.yml
└── requirements.txt
```

---

## 🚀 Getting Started

### Option A — Docker (Recommended)

```bash
git clone https://github.com/your-username/backend-projects.git
cd backend-projects/student-management-system
docker compose up --build
```

| Service | URL |
|---------|-----|
| Frontend UI | http://localhost:8000/app |
| API Docs | http://localhost:8000/docs |
| Monitoring | http://localhost:8000/monitoring/dashboard |

### Option B — Local

```bash
pip install -r requirements.txt
uvicorn App.Main:app --reload
```

---

## 📡 API Endpoints

### Authentication
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/auth/register` | Register a new user |
| POST | `/auth/login` | Login and get JWT token |

### Students
| Method | Endpoint | Role Required |
|--------|----------|--------------|
| GET | `/students/` | Any logged-in user |
| GET | `/students/{id}` | Any (students see own only) |
| POST | `/students/` | Admin only |
| PUT | `/students/{id}` | Admin or own profile |
| DELETE | `/students/{id}` | Admin only |

---

## 🧪 Running Tests

```bash
pytest Tests/ -v
```

---

## 🔒 Roles & Permissions

| Action | Admin | Student |
|--------|-------|---------|
| View all students | ✅ | ✅ |
| Create student | ✅ | ❌ |
| Update own profile | ✅ | ✅ |
| Delete student | ✅ | ❌ |

---
