# 🗂️ MySQL Helpdesk Ticket System (CMD-Based Case Study)

## 📘 Overview

This case study demonstrates how to create and manage a basic helpdesk ticketing system using **MySQL through Command Prompt (CMD)** on a Windows 10 virtual machine. It simulates realistic IT support tasks such as creating databases, managing records, and running SQL queries—all from the command line.

---

## 🔧 Tools Used

- MySQL Server on Windows
- Windows 10 Virtual Machine
- Command Prompt (CMD)

---

## 🧪 Scenario

> Simulate an internal helpdesk system where IT support staff can manage support tickets.

---

## 🛠️ Tasks Performed

### 1. Log in to MySQL
```bash
mysql -u root -p

### 2. Create and Use a Database
CREATE DATABASE itsupport;
USE itsupport;

### 3.  Create a Tickets Table
CREATE TABLE tickets (
  id INT AUTO_INCREMENT PRIMARY KEY,
  username VARCHAR(100),
  issue VARCHAR(255),
  status VARCHAR(50)
);

### 4. Insert Records
INSERT INTO tickets (username, issue, status)
VALUES
('jane.doe', 'Printer not responding', 'open'),
('john.doe', 'PC not booting', 'open'),
('Alex.hudson', 'WI-FI not connecting', 'open');

### 5. Query Records
SELECT * FROM tickets;

### 6. Update a Ticket
UPDATE tickets SET status = 'closed' WHERE id = 1;

### 7. Delete a Ticket
DELETE FROM tickets WHERE id = 2;

---

## ✅ Outcome

-Successfully created and managed a basic ticketing table using SQL
-Practiced full CRUD operations (Create, Read, Update, Delete)
-Gained experience working with MySQL via the command line


## 💡 Key Learnings

-How to interact with MySQL databases without a GUI
-How to structure tables and use SQL statements
-How command-line tools are used in real-world IT environments

