# 📚 Student Database Console App (Java + JDBC + MySQL)

## 📝 Description
This project is a simple **console-based Java application** for managing student records using **JDBC** and **MySQL**.  
It demonstrates basic CRUD operations:

- ➕ Add a student  
- ✏️ Update a student  
- ❌ Delete a student  
- 🔍 View a student by ID  
- 📃 List all students  

It’s a beginner-friendly project to practice **Java + MySQL integration**.

---

## ⚙️ Setup Instructions

### 1. Requirements
- Java 8 or later  
- MySQL server installed  
- MySQL Connector/J (JDBC driver) – `mysql-connector-j-9.4.0.jar`

---

### 2. Database Setup
1. Open MySQL Workbench or terminal.  
2. Run the following SQL script:


CREATE DATABASE studentdb;

USE studentdb;

CREATE TABLE students (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    dob DATE NOT NULL
);

### 3. Configure Database Connection
Update your MySQL credentials in DBConnection.java:

### 4. Compile and Run
Windows (PowerShell / CMD)
powershell
Copy code
javac -cp ".;mysql-connector-j-9.4.0.jar" *.java
java -cp ".;mysql-connector-j-9.4.0.jar" Main

📌 Notes & Assumptions
Date of birth must be entered in YYYY-MM-DD format.

Email has a UNIQUE constraint → duplicate emails are not allowed.

The app is console-only (no GUI).

Click ▶️ to launch from inside VS Code.
