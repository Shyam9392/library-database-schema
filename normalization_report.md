# Normalization Report

## Library Management System – Normalization Steps

This report explains how the tables in this project achieve the three main normal forms (1NF, 2NF, 3NF).

---

## 1. First Normal Form (1NF)

- All tables have a primary key.
- Each field contains only atomic (single) values.
- No repeating groups or arrays exist in any table.

**Examples:**
- In `book`, each row refers to a single book with individual attributes (one title, one author_id).
- In `borrowed_book`, each record represents a single book borrowed in a transaction (not a list of books).

---

## 2. Second Normal Form (2NF)

- The tables that have a composite primary key (like `borrowed_book`) have all non-key columns fully dependent on the whole composite key.
- In tables with single-column primary keys, 2NF is already satisfied.

**Examples:**
- In `borrowed_book`, both `transaction_id` and `book_id` together identify each row, and no other attribute depends on only part of this key.
- In `book`, all fields depend on `isbn` (the primary key).

---

## 3. Third Normal Form (3NF)

- No transitive dependencies: Non-key columns depend only on the primary key, not on another non-key column.

**Examples:**
- In `author`, `name` depends only on `author_id`.
- In `book`, `author_id` is a foreign key but isn’t derived from any other non-key column.
- In `transaction`, `transaction_date` depends only on `transaction_id`, and not on `patron_id`.

---

**Summary:**  
All tables are designed to ensure atomicity, eliminate partial and transitive dependencies, and conform to 3NF for efficient and reliable data management.