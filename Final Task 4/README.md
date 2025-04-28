# Finals Task 4 - Employee Databases


## Task Overview

This project covers the following key areas:

- Creation of two databases: `payroll` and `employeeDB`
- Designing tables: `EmployeeSalaries` and `EmployeeData`
- Inserting sample data into the tables
- Writing and executing SQL queries to solve practical problems

---

## Database Structures

### Problem 1: Payroll Database

**Database:** `payroll`

**Table:** `EmployeeSalaries`
```sql
CREATE DATABASE payroll;
USE payroll;

CREATE TABLE EmployeeSalaries (
  employee_id INT AUTO_INCREMENT PRIMARY KEY,
  employee_name VARCHAR(100),
  department VARCHAR(50),
  salary DECIMAL(10,2),
  hire_date DATE
);
```

**Sample Data:**
- Includes employees across Sales, Marketing, HR, and IT departments.
- Salaries and hire dates are provided.

---

### Problem 2: Employee Management Database

**Database:** `employeeDB`

**Table:** `EmployeeData`
```sql
CREATE DATABASE employeeDB;
USE employeeDB;

CREATE TABLE EmployeeData (
  employee_id INT AUTO_INCREMENT PRIMARY KEY,
  full_name VARCHAR(100),
  department VARCHAR(50),
  salary DECIMAL(10,2),
  hire_date DATE,
  manager_id INT
);
```

**Sample Data:**
- Includes employee-manager relationships.
- Salaries range from 60,000 to 193,000.

---

## SQL Query Exercises

### Problem 1 Queries
```sql
-- List of employees and salaries in descending order
SELECT employee_name, salary FROM EmployeeSalaries ORDER BY salary DESC;

-- Average salary by department
SELECT department, AVG(salary) AS average_salary FROM EmployeeSalaries GROUP BY department;
```

### Problem 2 Queries
```sql
-- Full names and salaries ordered by highest salary
SELECT full_name, salary FROM EmployeeData ORDER BY salary DESC;

-- Average salary filter over 70,000
SELECT AVG(salary) AS average_salary FROM EmployeeData HAVING average_salary > 70000;

-- Full names of employees earning more than 100,000
SELECT full_name FROM EmployeeData WHERE salary > 100000;

-- Count the total number of employees
SELECT COUNT(employee_id) AS number_of_employees FROM EmployeeData;
```
