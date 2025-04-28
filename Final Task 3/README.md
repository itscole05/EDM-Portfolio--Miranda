# Final Lab Task 3: Table Manipulation #

## Task 1 - SQL Query Operations

```sql
SELECT * FROM products_tbl;
DESCRIBE products_tbl;
```

---

## Task 2 - Defining the Table Structure

```sql
CREATE DATABASE products_db;
USE products_db;

CREATE TABLE products_tbl (
    id INT AUTO_INCREMENT PRIMARY KEY,
    product_name VARCHAR(100) NOT NULL,
    price DECIMAL(10, 2)
);

ALTER TABLE products_tbl
ADD CONSTRAINT chk_price CHECK (price > 0);

INSERT INTO products_tbl (product_name, price)
VALUES
    ('Laptop', 999.99),
    ('Smartphone', 599.99),
    ('Tablet', 299.99),
    ('Keyboard', 19.99),
    ('Mouse', 14.99),
    ('Desk Lamp', 24.99),
    ('Speakers', 9.99);

ALTER TABLE products_tbl
MODIFY COLUMN product_name VARCHAR(120) NOT NULL;
```

---

## Task 3 - Schema Diagram for Products Table

<img src="https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%203/Imagesft3/tables%20(2).png" alt="Alt Text" width="800" height="400">

---

## Task 4 - Raw SQL Script for Database and Table

[Raw Copy of MySQL File](https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Final%20Task%203/Imagesft3/products_db_products.sql)

```sql
CREATE DATABASE products_db;
USE products_db;

CREATE TABLE products_tbl (
    id INT AUTO_INCREMENT PRIMARY KEY,
    product_name VARCHAR(100) NOT NULL,
    price DECIMAL(10, 2)
);

ALTER TABLE products_tbl
ADD CONSTRAINT chk_price CHECK (price > 0);

INSERT INTO products_tbl (product_name, price)
VALUES
    ('Laptop', 999.99),
    ('Smartphone', 599.99),
    ('Tablet', 299.99),
    ('Keyboard', 19.99),
    ('Mouse', 14.99),
    ('Desk Lamp', 24.99),
    ('Speakers', 9.99);

ALTER TABLE products_tbl
MODIFY COLUMN product_name VARCHAR(120) NOT NULL;

SELECT * FROM products_tbl;
DESCRIBE products_tbl;
```
