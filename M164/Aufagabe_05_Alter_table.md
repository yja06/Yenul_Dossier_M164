# Einrichtung und Modifikation der Datenbank `company`

```sql
CREATE DATABASE IF NOT EXISTS company;

USE company;

CREATE TABLE employees (
    id INT AUTO_INCREMENT PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    email VARCHAR(100),
    hire_date DATE,
    salary DECIMAL(10,2)
);

ALTER TABLE employees
ADD COLUMN department VARCHAR(50);

ALTER TABLE employees
MODIFY COLUMN salary FLOAT(10,2);

ALTER TABLE employees
CHANGE COLUMN department department_id VARCHAR(50);

ALTER TABLE employees
MODIFY COLUMN department_id INT;

ALTER TABLE employees
DROP COLUMN email;
