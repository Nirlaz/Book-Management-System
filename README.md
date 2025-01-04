# Book Management System

## Description
A full-stack Book Management System built with React for the frontend, Java Servlets for the backend, and MySQL for database management. This system allows users to perform CRUD operations on books, such as adding, updating, deleting, and viewing book details.

## Features
- Add new books
- View and search the list of books
- Edit existing book details
- Delete books
- MySQL database for data storage
- User-friendly interface with React

## Tech Stack
- **Frontend**: React.js
- **Backend**: Java Servlets
- **Database**: MySQL

## Getting Started

### Prerequisites
Make sure you have the following installed:
- **Node.js** for React development
- **Java Development Kit (JDK)** for Servlets
- **MySQL** for database management
- **Apache Tomcat** for running the Servlets
### Fronend
###(Display Books)
![image](https://github.com/user-attachments/assets/7213b79e-4176-4c01-8754-650751fbd085)

 
###(For Adding Books)
 ![image](https://github.com/user-attachments/assets/87d7d7c6-fd5a-4b3b-a6ef-718b449cf2f7)

 
-----
**Add a New Book**

- **Endpoint**: /add
- **Method**: POST
- **Description**: Adds a new book to the database with the provided bookName and isbn.
![image](https://github.com/user-attachments/assets/7059281f-ad03-4d0b-b007-4dff2985c259)



- **Failure**:
  - Status: 500 Internal Server Error
  - Content:

![image](https://github.com/user-attachments/assets/6897c62f-949b-4263-a8e9-048dc6e5c8e0)


**Error Handling:**

- **Missing fields**: If bookName or isbn is missing, a 400 Bad Request error will be returned.
-----
**Get List of Books**

- **Endpoint**: /books
- **Method**: GET
- **Description**: Fetches a list of all books in the database.

**Response:**

- **Success**:
  - Status: 200 OK
  - Content:
![image](https://github.com/user-attachments/assets/0fe66b7e-fef5-4d47-81c9-cd52a9aa06a5)


**Delete a Book**

- **Endpoint**: /delete
- **Method**: POST
- **Description**: Deletes the book with the specified id from the database.

**Request Body (JSON):**

**Response:**

- **Success**:
  - Status: 200 OK
  - Content:
![image](https://github.com/user-attachments/assets/735fb25d-a228-4c23-a03c-f87c3b20a188)


**Failure**:
  - Status: 500 Internal Server Error
  - Content:
- **If Book Not Found**:
  - Status: 404 Not Found
  - Content:

![image](https://github.com/user-attachments/assets/6c4bb407-3b48-4d1e-a195-6539943b8049)

-----
**General Notes**

- All interactions require the JSON format for the request body.
- The server uses **Hibernate** to interact with a MySQL database. Configuration for the database is specified in hibernate.cfg.xml.
- The book data is stored in the Books entity with attributes id, bookName, and isbn.
- The methods return appropriate JSON responses based on the action performed.
-----
**Error Handling**

- Internal errors or database issues are communicated via 500 Internal Server Error status with a message indicating the failure.
- Missing fields or invalid inputs (e.g., missing book id for deletion) will result in a 400 Bad Request error.





