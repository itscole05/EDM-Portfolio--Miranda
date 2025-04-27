# Finals Lab Task 2 - Transforming ER into Relational Tables

---

## Task 1 - Query Statements


SELECT * FROM student;
SELECT * FROM assignment;
SELECT * FROM submission;


---

## Task 2 - Table Structure and Insert Data

```sql
CREATE DATABASE student_db;
USE student_db;

CREATE TABLE student (
    username VARCHAR(50) PRIMARY KEY
);

CREATE TABLE assignment (
    shortname VARCHAR(50) PRIMARY KEY,
    due_date DATE NOT NULL,
    url VARCHAR(255) DEFAULT NULL
);

CREATE TABLE submission (
    username VARCHAR(50),
    shortname VARCHAR(50),
    version INT,
    submit_date DATE NOT NULL,
    data TEXT,
    PRIMARY KEY (username, shortname, version),
    FOREIGN KEY (username) REFERENCES student(username)
        ON DELETE CASCADE
        ON UPDATE CASCADE,
    FOREIGN KEY (shortname) REFERENCES assignment(shortname)
        ON DELETE CASCADE
        ON UPDATE CASCADE
);
```

---

## Task 2.1 - Insert Sample Data

```sql
INSERT INTO student (username) VALUES 
('Alexander Hamilton');

INSERT INTO assignment (shortname, due_date, url) VALUES 
('HIST101', '2025-04-30', 'http://assignments.com/hist101'), 
('GOVT201', '2025-05-15', 'http://assignments.com/govt201');

INSERT INTO submission (username, shortname, version, submit_date, data) VALUES 
('Alexander Hamilton', 'HIST101', 1, '2025-04-29', 'First submission for History'),
('Alexander Hamilton', 'HIST101', 2, '2025-04-30', 'Updated History submission'),
('Alexander Hamilton', 'GOVT201', 1, '2025-05-14', 'Government submission');
```

---

## Task 3 - Show Tables

```sql
SHOW TABLES;
```

---

## Task 4 - ER Diagram / Schema

 <img src="" alt="Alt Text" width="800" height="400"> 