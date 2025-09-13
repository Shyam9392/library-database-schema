# Library Database Schema (Internship Project)

This repository contains the **SQL schema** for a Library Management System as part of my internship project. The design follows best practices for database normalization up to 3NF.

## 📁 Contents

- `author.sql` &nbsp;→ Table for storing authors
- `book.sql`   &nbsp;&nbsp;→ Table for storing books and their authors
- `patron.sql` → Table for library patrons
- `transaction.sql` → Table to record borrow/return events
- `borrowed_book.sql` → Associates transactions with the books borrowed

## 🏗️ Schema Overview

- Efficiently manages authors, books, patrons, and borrowing records
- Foreign key constraints maintain referential integrity
- Fully normalized (up to 3NF)

## 📋 How to Use

1. **Run the `.sql` files** in order using pgAdmin or psql:
    - `author.sql` → `book.sql` → `patron.sql` → `transaction.sql` → `borrowed_book.sql`
2. Test queries using `SELECT` statements or by joining tables for reporting.

## 🎯 Project Goals

This structure:
- Demonstrates efficient relational design
- Prevents data redundancy
- Supports common operations for libraries

## 📝 Notes

- Database platform: PostgreSQL
- Designed as part of an internship learning project

---

Feel free to clone or fork this repository!

## contact 
For any questions contact:[shyamsunderkalyanapu@gmail.com]