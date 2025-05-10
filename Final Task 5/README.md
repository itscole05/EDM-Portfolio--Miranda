# Final Lab Task 5. Using SQL views and Stored Procedures and Stored Functions #

1. CREATE A VIEW that will display the vendors_code, vendors name, product description p_indate, of all products with p_indate from 2002 onwards

```sql
CREATE VIEW Q1 AS 
SELECT vendors.V_CODE, vendors.V_NAME, products.P_DESCRIPT, products.P_INDATE
FROM vendors
JOIN products ON vendors.V_CODE = products.V_CODE
WHERE products.P_INDATE >= '2002-01-01';

SELECT * FROM Q1;
```

**Output**
<img src="" alt="Alt Text" width="800" height="400"> 

2. CREATE a VIEW that will display all products whose price range is between 100-150

```sql
CREATE VIEW Q2 AS
SELECT P_DESCRIPT, P_PRICE
FROM products
WHERE P_PRICE BETWEEN 100 AND 150;

SELECT * FROM Q2;
```
**Output**
<img src="" alt="Alt Text" width="800" height="400"> 

3. Create a VIEW that will COMPUTE for the (TOTAL_PRICE) of ALL PRODUCTS by getting the (P_ONHAND x P_PRICE) Sold by vendors with the following v_code (21344, 23119 and 24288)

```sql
CREATE VIEW Q3 AS
SELECT SUM(P_ONHAND * P_PRICE) AS total_price
FROM products
WHERE V_CODE IN (21344, 23119 and 24288);

SELECT * FROM Q3;

DELIMITER $$
```
**Output**
<img src="" alt="Alt Text" width="800" height="400"> 

4.CREATE a STORED PROCEDURE that WILL take a SINGLE PARAMETER and UPDATED the Name of Vendor ‘Bryson,Inc.’ to ‘Bryson and Co’.

```sql
CREATE PROCEDURE Q4(IN old_name VARCHAR(30))
BEGIN 
UPDATE vendors
SET V_NAME = 'Bryson and Co.'
WHERE V_NAME = old_name;
SELECT * FROM vendors WHERE V_NAME = 'Bryson and Co.';
END $$
DELIMITER ;
```
**Output**
<img src="" alt="Alt Text" width="800" height="400"> 

5. CREATE A Function that will take 2 parameters(v_code and v_state) and display All the product description and price based on the parameters passed to the function.

```sql 
SELECT Q5(21344, 'KY');
```
**Output**
<img src="" alt="Alt Text" width="800" height="400"> 


[MYSQL FILE LAB TASK 5 ](.)

