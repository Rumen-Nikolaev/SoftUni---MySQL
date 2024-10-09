# Basic CRUD in MySQL Server

## Create, Retrieve, Update, Delete – Using SQL Queries
**SoftUni Team**  
**Technical Trainers**  
**Software University**  
[SoftUni](https://softuni.bg)

---

## Table of Contents
1. [Query Basics](#query-basics)
2. [Retrieving Data](#retrieving-data)
3. [Writing Data in Tables](#writing-data-in-tables)
4. [Modifying Existing Records](#modifying-existing-records)

---

## Query Basics
### SQL Introduction
### SQL Queries – Few Examples (1)
- Select first, last name and job title about employees:
  ```sql
  SELECT first_name, last_name, job_title FROM employees;


-- Query Basics
-- SQL Introduction

-- SQL Queries – Few Examples (1)
-- Select first, last name and job title about employees:
SELECT first_name, last_name, job_title FROM employees;

-- Select projects which start on 01-06-2003:
SELECT * FROM projects WHERE start_date = '2003-06-01';

-- Inserting data into table:
INSERT INTO projects(name, start_date)
VALUES('Introduction to SQL Course', '2006-01-01');

-- SQL Queries – Few Examples (2)
-- Update end date of specific projects:
UPDATE projects
SET end_date = '2006-08-31'
WHERE start_date = '2006-01-01';

-- Delete specific projects:
DELETE FROM projects
WHERE start_date = '2006-01-01';

-- Retrieving Data
-- Using SQL SELECT

-- Capabilities of SQL SELECT
-- Projection: Take a subset of the columns
-- Selection: Take a subset of the rows
-- Join: Combine tables by some column

-- SELECT – Examples
-- Selecting all columns from the "employees" table
SELECT * FROM employees;

-- Problem: Select Employee Information
-- Write a query to select all employees from "Hotel" database
-- Retrieve information about their id, first_name, last_name and job_title
-- Ordered by id

-- Solution: Select Employee Information
SELECT id, first_name, last_name, job_title
FROM employees
ORDER BY id;

-- Aliases rename a table or a column heading:
SELECT e.id AS 'No.',
       e.first_name AS 'First Name',
       e.last_name AS 'Last Name',
       e.job_title AS 'Job Title'
FROM employees AS e 
ORDER BY id;

-- Concatenation (1)
-- `concat()` - returns the string that results from concatenating the arguments
-- String literals are enclosed in `['`](single quotes)
-- Table and column names containing special symbols use [`] (backtick)
SELECT concat(`first_name`, ' ', `last_name`) AS 'full_name',
       `job_title` AS 'Job Title',
       `id` AS 'No.'
FROM `employees`;

-- Concatenation (2)
-- Another function of concatenation is `concat_ws()` - stands for concatenate with separator and is a special form of CONCAT()
SELECT concat_ws(' ', `first_name`, `last_name`, `job_title`) AS 'full_name',
       `job_title` AS 'Job Title',
       `id` AS 'No.'
FROM `employees`;
-- Skip any NULL values after the separator argument.

-- Problem: Select Employees with Filter
-- Find information about all employees, listing their:
-- Full Name
-- Job title
-- Salary
-- Use concatenation to display first and last names as one field

-- Solution: Select Employees with Filter
SELECT concat(`first_name`, ' ', `last_name`) AS 'Full name',
       `job_title` AS 'Job title',
       `salary` AS 'Salary'
FROM `employees` 
WHERE salary > 1000;

-- Filtering the Selected Rows
-- Use `DISTINCT` to eliminate duplicate results
SELECT DISTINCT `department_id`
FROM `employees`;

