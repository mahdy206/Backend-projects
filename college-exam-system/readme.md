# 📝 College Exam System

A desktop application built with **Java** and **JavaFX** for managing college exams, featuring role-based dashboards for Admins, Lecturers, and Students with full file-based data persistence.

---

## ✨ Features

- 🔐 **Role-Based Login** — Admin, Lecturer, and Student dashboards
- 👨‍💼 **Admin Panel** — Add/update/delete students, lecturers, subjects, and assign roles
- 👨‍🏫 **Lecturer Panel** — Create, update, and delete exams with custom questions
- 🎓 **Student Panel** — Take exams and view scores
- 💾 **File Persistence** — All data saved and loaded from local `.txt` files
- 🎨 **Modern UI** — Gradient-styled JavaFX interface

---

## 🛠️ Tech Stack

| Category | Technology |
|----------|-----------|
| Language | Java |
| GUI | JavaFX |
| Storage | File I/O (txt files) |
| Build | Standard Java |

---

## 👥 User Roles

### Admin
- Add / update / delete Students and Lecturers
- Add Subjects and assign them to users
- Search users by username

### Lecturer
- Add / update / delete Exams
- View assigned subjects
- Each exam has 3 questions with correct answers

### Student
- Take exams by entering Subject ID
- View scores per subject

---

## 🚀 Getting Started

### Prerequisites
- Java 11+
- JavaFX SDK

### Run

```bash
javac --module-path /path/to/javafx/lib --add-modules javafx.controls,javafx.fxml CollegeExamSystem.java
java --module-path /path/to/javafx/lib --add-modules javafx.controls,javafx.fxml CollegeExamSystem
```

> Default admin credentials: **username:** `admin` | **password:** `admin123`

---

## 💾 Data Files Generated

| File | Content |
|------|---------|
| `students.txt` | Student records |
| `lecturers.txt` | Lecturer records |
| `admin.txt` | Admin accounts |
| `subjects.txt` | Subject list |
| `exams.txt` | Exam questions and answers |
| `scores.txt` | Student scores per subject |

---

## 📁 Project Structure

```
college-exam-system/
├── CollegeExamSystem.java    ← Main application file
└── README.md
```

---

## 📦 Code Files

<!-- Add your project files here -->CollegeExamSystem.java
