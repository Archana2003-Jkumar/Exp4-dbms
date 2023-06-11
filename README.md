# Exp4-dbms
## AIM
To create an SQL query to show record from one table that another table does not have.

## ALGORITHM 
### Steps
1.Create two tables named "table1" and "table2". Both tables have the same columns: id, name, department, and salary.
2.Insert sample data into both tables.
3.Use the SELECT statement with a NOT IN subquery to retrieve records from table1 that do not exist in table2 based on the id column comparison.
4.Retrieve the records from table1 that are not present in table2 based on the id column comparison.
5.End the program
## PROGRAM
```
--- Create the first table
CREATE TABLE table1 (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    department VARCHAR(50),
    salary DECIMAL(10, 2)
);

-- Create the second table
CREATE TABLE table2 (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    department VARCHAR(50),
    salary DECIMAL(10, 2)
);

-- Insert sample data into the first table
INSERT INTO table1 (id, name, department, salary)
VALUES (1, 'John Doe', 'Sales', 5000),
       (2, 'Jane Smith', 'Marketing', 6000),
       (3, 'David Johnson', 'IT', 7000),
       (4, 'Emily Brown', 'Finance', 5500),
       (5, 'Michael Davis', 'HR', 4500);

-- Insert sample data into the second table
INSERT INTO table2 (id, name, department, salary)
VALUES (1, 'John Doe', 'Sales', 5000),
       (3, 'David Johnson', 'IT', 7000),
       (5, 'Michael Davis', 'HR', 4500);

-- Retrieve records from table1 that do not exist in table2
SELECT *
FROM table1
WHERE id NOT IN (
    SELECT id
    FROM table2
);
```
## OUTPUT
![image](https://github.com/Archana2003-Jkumar/Exp4-dbms/assets/93427594/9e8e01eb-4a54-426b-8820-9e1617919783)

## RESULT
Thus an SQL query is implemented to show record from one table that another table does not have.
