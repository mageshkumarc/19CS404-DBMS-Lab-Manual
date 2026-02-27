# Experiment 3: DML Commands

## AIM
To study and implement DML (Data Manipulation Language) commands.

## THEORY

### 1. INSERT INTO
Used to add records into a relation.
These are three type of INSERT INTO queries which are as
A)Inserting a single record
**Syntax (Single Row):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES (value_1, value_2, ...);
```
**Syntax (Multiple Rows):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES
(value_1, value_2, ...),
(value_3, value_4, ...);
```
**Syntax (Insert from another table):**
```sql
INSERT INTO table_name SELECT * FROM other_table WHERE condition;
```
### 2. UPDATE
Used to modify records in a relation.
Syntax:
```sql
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
```
### 3. DELETE
Used to delete records from a relation.
**Syntax (All rows):**
```sql
DELETE FROM table_name;
```
**Syntax (Specific condition):**
```sql
DELETE FROM table_name WHERE condition;
```
### 4. SELECT
Used to retrieve records from a table.
**Syntax:**
```sql
SELECT column1, column2 FROM table_name WHERE condition;
```
**Question 1**
--
<img width="600" height="583" alt="image" src="https://github.com/user-attachments/assets/f484bdba-c3d9-4bdc-82e9-5c568a08dde4" />


```
SELECT
    id,
    value1,
    ABS(value1) AS 'absolute_value'
FROM Calculations
```

**Output:**

<img width="826" height="221" alt="image" src="https://github.com/user-attachments/assets/1d8d4212-bfd1-42cf-a78c-35b3de84b128" />

**Question 2**
---
<img width="600" height="583" alt="image" src="https://github.com/user-attachments/assets/21110155-a7f9-4eef-a5a3-bd821a65092a" />


```
UPDATE Employees
SET SALARY=SALARY*2
WHERE DEPARTMENT_ID=20 AND JOB_ID LIKE "%MAN"
```

**Output:**

<img width="826" height="268" alt="image" src="https://github.com/user-attachments/assets/6becc373-4883-4391-9691-cc1bc409cd5c" />

**Question 3**
---
<img width="600" height="583" alt="image" src="https://github.com/user-attachments/assets/b48aaae1-b864-462c-9809-cdfc5ac4078f" />


```
UPDATE Employees
SET EMAIL='not available',COMMISSION_PCT=0.55
WHERE DEPARTMENT_ID=110
```

**Output:**

<img width="826" height="314" alt="image" src="https://github.com/user-attachments/assets/8a344b01-6d67-457a-8c01-b957f8ad0f8a" />


**Question 4**
---
<img width="600" height="583" alt="image" src="https://github.com/user-attachments/assets/373b9361-533d-4152-873f-bd7273da1fdf" />


```
UPDATE products
SET product_name='Grapefruit'
WHERE product_id=4
```

**Output:**

<img width="826" height="218" alt="image" src="https://github.com/user-attachments/assets/8696cade-e4f9-45d0-bac1-efa068b8662a" />


**Question 5**
---
<img width="600" height="583" alt="image" src="https://github.com/user-attachments/assets/4b475ce3-b374-4700-a046-2bcabcf1fb75" />


```
SELECT
    id,
    value2,
    CASE
        WHEN value2<10 THEN 'Small'
        WHEN value2>=10 AND value2<=50 THEN 'Medium'
        WHEN value2>50 THEN 'Large'
    END AS size_category
FROM Calculations
```

**Output:**

<img width="826" height="230" alt="image" src="https://github.com/user-attachments/assets/924679c2-4b4c-4042-b0ad-703d8dbe8360" />


**Question 6**
---
<img width="600" height="568" alt="image" src="https://github.com/user-attachments/assets/7a61b62c-00f8-4ffb-a820-cce7b9b20a38" />


```
SELECT 
    ename,
    hiredate,
    CASE strftime("%w",hiredate)
        WHEN '0' THEN 'Sunday'
        WHEN '1' THEN 'Monday'
        WHEN '2' THEN 'Tuesday'
        WHEN '3' THEN 'Wednesday'
        WHEN '4' THEN 'Thursday'
        WHEN '5' THEN 'Friday'
        WHEN '6' THEN 'Saturday'
    END AS day_of_week
FROM emp
```

**Output:**

<img width="1460" height="567" alt="image" src="https://github.com/user-attachments/assets/d5b4525b-236b-4801-8090-4df9d29b5ba1" />

**Question 7**
---
-- Paste Question 7 here

```sql
-- Paste your SQL code below for Question 7
```

**Output:**

![Output7](output.png)

**Question 8**
---
-- Paste Question 8 here

```sql
-- Paste your SQL code below for Question 8
```

**Output:**

![Output8](output.png)

**Question 9**
---
-- Paste Question 9 here

```sql
-- Paste your SQL code below for Question 9
```

**Output:**

![Output9](output.png)

**Question 10**
---
-- Paste Question 10 here

```sql
-- Paste your SQL code below for Question 10
```

**Output:**

![Output10](output.png)

## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
