# Hostel Management System

**C Language | File Handling | Role-Based Authentication**

A menu-driven Hostel Management System developed in **C** that allows a **Warden (Admin)** and **Students** to securely manage hostel operations using **file-based storage**.

This project simulates a **real-world hostel ERP system** using **structures, functions, file handling, authentication, and role-based access**.

---

## 📌 Problem Statement

Manual hostel record keeping leads to:

- Data loss
- No security
- Poor management
- No tracking of rooms, fees, or complaints

This system automates hostel management with:

- Secure login
- Permanent data storage
- Separate roles for Admin and Students

---

## 👥 System Users

| User               | Description                                        |
| ------------------ | -------------------------------------------------- |
| **Admin (Warden)** | Has full control over hostel data                  |
| **Student**        | Can view own data, pay fees, and submit complaints |

---

## 🔐 Authentication & Authorization

Users must log in using **ID and password**.

| Feature           | Admin | Student |
| ----------------- | ----- | ------- |
| Add student       | ✔     | ❌      |
| View all students | ✔     | ❌      |
| Assign rooms      | ✔     | ❌      |
| View fees         | ✔     | ❌      |
| Submit complaint  | ❌    | ✔       |
| View own data     | ❌    | ✔       |

This ensures **security and role-based access control**.

---

## 🧱 Software Architecture

```
User
  ↓
Menu System
  ↓
Login & Authentication
  ↓
Role Validation (Admin / Student)
  ↓
Function Execution
  ↓
File Read / Write
  ↓
Data Display
```

---

## 📂 File-Based Database Design

| Data       | File           |
| ---------- | -------------- |
| Students   | students.dat   |
| Admins     | admins.dat     |
| Rooms      | rooms.dat      |
| Fees       | fees.dat       |
| Complaints | complaints.dat |

Each file behaves like a **database table**.

---

## 🧩 Data Structures

```c
struct Student {
    int id;
    char name[50];
    char password[20];
    int roomNo;
};

struct Admin {
    char username[20];
    char password[20];
};

struct Room {
    int roomNo;
    int capacity;
    int occupied;
};

struct Fee {
    int studentId;
    float total;
    float paid;
};

struct Complaint {
    int studentId;
    char text[200];
};
```

---

## 📊 Data Flow

```
User Input
    ↓
Menu Selection
    ↓
Authentication
    ↓
Role Check
    ↓
Function Execution
    ↓
File Access
    ↓
Result Display
```

---

## 🗂 Folder Structure

```
hostel-management-system/
│
├── main.c
│
├── headers/
│   ├── student.h
│   ├── admin.h
│   ├── room.h
│   ├── fee.h
│   └── complaint.h
│
├── data/
│   ├── students.dat
│   ├── admins.dat
│   ├── rooms.dat
│   ├── fees.dat
│   └── complaints.dat
│
├── docs/
│   ├── flowchart.png
│   ├── er-diagram.png
│   └── screenshots/
│
└── README.md
```

---

## 🧠 Menu System

### Main Menu

```
1. Admin Login
2. Student Login
3. Exit
```

### Admin Menu

```
1. Add Student
2. View Students
3. Assign Room
4. View Fees
5. View Complaints
6. Delete Student
7. Logout
```

### Student Menu

```
1. View My Details
2. Pay Fees
3. Submit Complaint
4. Logout
```

---

## 🛠 Task List

### Phase 1 – Core System

- Login system
- Student registration
- File handling

### Phase 2 – Hostel Logic

- Room allocation
- Fee management

### Phase 3 – Role Control

- Admin & student permissions
- Secure access

### Phase 4 – Complaints

- Student complaint system
- Admin viewing

### Phase 5 – Finalization

- Testing
- Screenshots
- Documentation

---
