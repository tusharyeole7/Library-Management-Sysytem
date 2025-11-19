# Library Management System 📚

A simple, efficient Command Line Interface (CLI) application designed to manage the day-to-day operations of a library. Built using **Python** for logic and **MySQL** for data persistence.

## 🚀 Features

* **Book Management:**
    * Add new books with details (ISBN, Title, Author, Quantity, Year).
    * Update existing book details.
    * Remove books from the inventory.
    * Search for books by keyword (Title or Author).
    * List all available books (Quantity > 0).
* **Member Management:**
    * Register new members (ID, Name, Email).
    * Remove members.
* **Circulation System:**
    * **Borrow Books:** Records the transaction, checks stock availability, and automatically decrements the book quantity.
    * **Return Books:** Updates the return date and automatically increments the stock quantity.
    * **History:** View a list of all borrowing records.

## 🛠️ Tech Stack

* **Language:** Python 3.x
* **Database:** MySQL Server
* **Libraries:** `mysql-connector-python`, `datetime`

## ⚙️ Database Schema

The system automatically initializes the following three tables:

1.  **Books:** Stores inventory details. Primary Key: `ISBN`.
2.  **Members:** Stores user information. Primary Key: `member_id`.
3.  **BorrowedBooks:** Tracks transactions, linking books and members. Primary Key: `borrow_id`.

## 📦 Installation & Setup

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/yourusername/repository-name.git](https://github.com/yourusername/repository-name.git)
    ```
2.  **Install required Python modules:**
    ```bash
    pip install mysql-connector-python
    ```
3.  **Database Configuration:**
    * Ensure your MySQL server is running.
    * Create a database named `Library` in your MySQL instance.
    * *Note: The script currently uses hardcoded credentials (`root` user and a password). For security, it is highly recommended to update the `connection()` function to read credentials from a secure environment file (`.env`).*

## 🖥️ Usage

Run the main script to start the application:

```bash
python Library.py
