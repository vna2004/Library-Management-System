# Library Management System

## Project Overview

This is a simple Library Management System built using Java Swing (NetBeans) for the graphical user interface (GUI) and MySQL for the database backend. The system allows the library staff to manage books, issue books, return books, track real-time transactions, and maintain records of students and staff.

## Features

- **Book Search**: Search for books by Book ID.
- **Issue Book**: Issue a book to a borrower with details such as book ID, book name, borrower ID, issue date, and due date.
- **Return Book**: Return a borrowed book and update its status.
- **View Books**: View a list of all available books in the library.
- **Real-time Transaction Tracking**: Track all transactions like issued books, returns, and due dates.
- **Students and Staff Records**: Maintain records of students and staff, including personal details and issued books.
- **Database Integration**: MySQL for storing and retrieving book and transaction data.
  
## Technologies Used

- **Java (Swing)**: Used for creating the GUI components.
- **NetBeans**: Integrated development environment (IDE) for developing the Java application.
- **MySQL**: Relational database management system (RDBMS) for managing book and transaction data.

## User Interface 
![Image](https://github.com/user-attachments/assets/173f3d4d-b839-4fa7-b3df-a756ce2fedba)

![Image](https://github.com/user-attachments/assets/85caf0f3-78da-4a90-a43b-24492b7b9b03)

## Database Setup

Ensure MySQL is installed and running on your local machine. The database schema is designed with tables for books, transactions, students, and staff.

### SQL Schema
```sql
CREATE DATABASE library;

USE library;

CREATE TABLE books (
  book_id INT PRIMARY KEY,
  book_name VARCHAR(255),
  author_name VARCHAR(255),
  availability_status VARCHAR(20) DEFAULT 'Available'
);

CREATE TABLE managebooks (
  book_id INT,
  book_name VARCHAR(255),
  borrower_id INT,
  issue_date DATE,
  due_date DATE,
  status VARCHAR(10)
);

CREATE TABLE students (
  student_id INT PRIMARY KEY,
  student_name VARCHAR(255),
  contact_details VARCHAR(255)
);

CREATE TABLE staff (
  staff_id INT PRIMARY KEY,
  staff_name VARCHAR(255),
  position VARCHAR(255),
  contact_details VARCHAR(255)
);
