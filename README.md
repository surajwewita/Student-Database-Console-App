# Student Database Console App (Java + JDBC + MySQL)

## 📌 Description
A simple **console-based Java application** to manage students using MySQL database.

Features:
- Add student
- Update student
- Delete student
- View student by ID
- List all students

---

## ⚙️ Setup Instructions

### 1. Database Setup
1. Open MySQL Workbench or terminal.
2. Run the SQL script:
   ```sql
   CREATE DATABASE studentdb;

   USE studentdb;

   CREATE TABLE students (
       id INT AUTO_INCREMENT PRIMARY KEY,
       name VARCHAR(100) NOT NULL,
       email VARCHAR(100) UNIQUE NOT NULL,
       dob DATE NOT NULL
   );
