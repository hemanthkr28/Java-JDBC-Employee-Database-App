Employee Database App
Project Overview

This is a Java JDBC application that connects to a MySQL/PostgreSQL database to perform CRUD operations on an Employee table.

Objective:

Master Java DB connectivity using JDBC.

Perform Create, Read, Update, Delete operations.

Tools & Technologies

Java 15 (or Java 8 for simplicity)

MySQL or PostgreSQL

Eclipse IDE / VS Code

JDBC Driver (MySQL Connector/J or PostgreSQL JDBC)

Maven (optional, if using Maven project)

Database Setup (MySQL Example)

Log in to MySQL:

mysql -u root -p


Create database:

CREATE DATABASE employee_db;
USE employee_db;


Create Employee table:

CREATE TABLE employees (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100) NOT NULL,
    position VARCHAR(100),
    salary DOUBLE
);

Project Structure
EmployeeDatabaseApp/
 ├── src/
 │    └── com/hemanth/jdbc/EmployeeDatabaseApp.java
 ├── lib/
 │    └── mysql-connector-java-8.x.x.jar
 ├── README.md

How to Run

Add JDBC Driver to Eclipse:

Right-click project → Build Path → Configure Build Path → Add External JARs → select the .jar file.

Update Database Credentials in Java Code:

static final String DB_URL = "jdbc:mysql://localhost:3306/employee_db";
static final String USER = "root";
static final String PASS = "your_password";


Run the Application:

Right-click EmployeeDatabaseApp.java → Run As → Java Application

Use the Menu to:

Add Employee

View Employees

Update Employee

Delete Employee

Exit

Notes

Ensure MySQL server is running.

Use --add-modules java.sql in VM arguments if using Java 9+ and facing module issues.

For PostgreSQL, update the JDBC URL and driver accordingly:

static final String DB_URL = "jdbc:postgresql://localhost:5432/employee_db";
static final String USER = "postgres";
static final String PASS = "your_password";

Outcome

After running the app, you can:

Connect Java to a relational database.

Perform CRUD operations.

Practice using Connection, PreparedStatement, and ResultSet effectively.
