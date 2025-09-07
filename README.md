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
2. Run the following SQL script (or use the included [`create_database.sql`](create_database.sql)):

```sql
CREATE DATABASE studentdb;

USE studentdb;

CREATE TABLE students (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    dob DATE NOT NULL
);
3. Configure Database Connection
Update your MySQL credentials in DBConnection.java:

java
Copy code
private static final String URL = "jdbc:mysql://localhost:3306/studentdb";
private static final String USER = "root";          // your MySQL username
private static final String PASSWORD = "your_pass"; // your MySQL password
4. Compile and Run
Windows (PowerShell / CMD)
powershell
Copy code
javac -cp ".;mysql-connector-j-9.4.0.jar" *.java
java -cp ".;mysql-connector-j-9.4.0.jar" Main
Linux / macOS (Terminal)
bash
Copy code
javac -cp ".:mysql-connector-j-9.4.0.jar" *.java
java -cp ".:mysql-connector-j-9.4.0.jar" Main
📌 Notes & Assumptions
Date of birth must be entered in YYYY-MM-DD format.

Email has a UNIQUE constraint → duplicate emails are not allowed.

The app is console-only (no GUI).

📂 Project Structure
css
Copy code
StudentApp/
│── Main.java
│── Student.java
│── StudentDAO.java
│── DBConnection.java
│── create_database.sql
│── mysql-connector-j-9.4.0.jar
│── README.md
🚀 How to Run in VS Code
Use the provided launch.json to include the MySQL connector JAR.

Select Run Main with MySQL in the Run/Debug dropdown.

Click ▶️ to launch from inside VS Code.

👨‍💻 Author
Developed by Suraj ✨
