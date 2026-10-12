# 📚 Online Book Store Database Management System

## 📌 Project Overview

The Online Book Store Database Management System is a SQL-based project developed using PostgreSQL. It manages book information, customer details, and order records in a relational database.

The project demonstrates practical SQL skills, including database creation, table relationships, data retrieval, filtering, joins, aggregate functions, grouping, and sales analysis.

## 🎯 Project Objectives

* Manage book inventory and book details.
* Store customer information.
* Maintain order records and purchase quantities.
* Analyze book sales and revenue.
* Identify popular books and frequent customers.
* Calculate remaining book stock.

## 🛠️ Technologies Used

* **Database:** PostgreSQL
* **Language:** SQL
* **Concepts:** Relational Database Management System (RDBMS)

## 🗂️ Database Structure

The database consists of three tables.

### 1. Books

Stores information about books available in the store.

| Column         | Data Type          | Description              |
| -------------- | ------------------ | ------------------------ |
| Book_ID        | SERIAL PRIMARY KEY | Unique ID for each book  |
| Title          | VARCHAR(100)       | Title of the book        |
| Author         | VARCHAR(100)       | Author's name            |
| Genre          | VARCHAR(50)        | Book genre               |
| Published_Year | INT                | Year of publication      |
| Price          | NUMERIC(10,2)      | Price of the book        |
| Stock          | INT                | Available stock quantity |

### 2. Customers

Stores customer information.

| Column      | Data Type          | Description                 |
| ----------- | ------------------ | --------------------------- |
| Customer_ID | SERIAL PRIMARY KEY | Unique ID for each customer |
| Name        | VARCHAR(100)       | Customer's name             |
| Email       | VARCHAR(100)       | Customer's email address    |
| Phone       | VARCHAR(15)        | Customer's phone number     |
| City        | VARCHAR(50)        | Customer's city             |
| Country     | VARCHAR(150)       | Customer's country          |

### 3. Orders

Stores information about customer orders.

| Column       | Data Type          | Description                       |
| ------------ | ------------------ | --------------------------------- |
| Order_ID     | SERIAL PRIMARY KEY | Unique ID for each order          |
| Customer_ID  | INT                | References Customers(Customer_ID) |
| Book_ID      | INT                | References Books(Book_ID)         |
| Order_Date   | DATE               | Date of the order                 |
| Quantity     | INT                | Number of books ordered           |
| Total_Amount | NUMERIC(10,2)      | Total amount of the order         |

## 🔗 Database Relationships

* The `Customer_ID` column in the Orders table references the Customers table.
* The `Book_ID` column in the Orders table references the Books table.
* These foreign keys establish relationships between customers, books, and orders.

## 💻 SQL Queries and Features

### Basic SQL Queries

The project includes queries to:

1. Retrieve all books belonging to the Fiction genre.
2. Find books published after 1950.
3. Retrieve customers from Canada.
4. Find orders placed in November 2023.
5. Calculate the total stock of books.
6. Identify the most expensive book.
7. Retrieve orders containing more than one book.
8. Find orders with a total amount exceeding $20.
9. Display all distinct book genres.
10. Identify the book with the lowest stock.
11. Calculate total revenue generated from orders.

### Advanced SQL Queries

The project also demonstrates:

1. Calculate the total number of books sold for each genre.
2. Find the average price of Fantasy books.
3. Identify customers who have placed at least two orders.
4. Find the most frequently ordered book.
5. Retrieve the top three most expensive Fantasy books.
6. Calculate the total quantity of books sold by each author.
7. Identify customers who spent more than $30 and their cities.
8. Find the customer who spent the most on orders.
9. Calculate the remaining stock quantity for each book based on recorded orders.

## 🧠 SQL Concepts Practiced

* CREATE TABLE and DROP TABLE
* Primary Keys and Foreign Keys
* SELECT and WHERE
* ORDER BY and LIMIT
* DISTINCT
* BETWEEN
* Aggregate Functions: SUM(), AVG(), MAX(), COUNT()
* INNER JOIN and LEFT JOIN
* GROUP BY and HAVING
* COALESCE()
* Data Filtering and Sorting
* Sales and Inventory Analysis

## ⚙️ How to Run the Project

### Prerequisites

Install PostgreSQL and use a PostgreSQL-compatible SQL editor, such as pgAdmin.

### Steps

1. Clone or download this repository.
2. Open your PostgreSQL query editor.
3. Create a database named `Online_Book_Store`.
4. Connect to the database.
5. Open the SQL script containing the table definitions and queries.
6. Execute the table creation statements.
7. Insert sample records into the Books, Customers, and Orders tables.
8. Run the SQL queries to explore the database and analyze the results.

**Note:** The current SQL script defines the tables and queries. Insert sample data before executing queries that require records to return meaningful results.

## 📊 Key Learning Outcomes

Through this project, I practiced:

* Designing a relational database with multiple related tables.
* Establishing relationships using primary and foreign keys.
* Writing SQL queries to retrieve and filter data.
* Applying joins to combine information from multiple tables.
* Using aggregate functions to analyze sales and revenue.
* Applying grouping and filtering to answer business questions.
* Analyzing book inventory and customer purchasing behavior.

## 🚀 Future Improvements

* Add sample datasets for books, customers, and orders.
* Implement constraints to validate prices, quantities, and stock.
* Create views for frequently used sales reports.
* Add indexes to improve query performance where appropriate.
* Develop a frontend application to interact with the database.
* Connect the database to a backend API.

## 👨‍💻 Author

**Divyanshu Gupta**

Project: Online Book Store Database Management System

Technology: PostgreSQL and SQL

---

⭐ This project was created for learning and practicing SQL and relational database concepts.
