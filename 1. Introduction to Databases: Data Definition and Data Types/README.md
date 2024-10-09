# Introduction to Databases

Welcome to the **Introduction to Databases** course offered by **Software University**. This course provides a comprehensive understanding of database concepts, focusing on relational database management systems (RDBMS) and SQL.

## Table of Contents

1. [Data Management](#data-management)
2. [Database Engine](#database-engine)
3. [Structured Query Language](#structured-query-language)
4. [MySQL](#mysql)
5. [Table Relationships](#table-relationships)
6. [Programmability](#programmability)
7. [Data Types in MySQL Server](#data-types-in-mysql-server)
8. [Database Modeling](#database-modeling)
9. [Basic SQL Queries](#basic-sql-queries)
10. [Table Customization](#table-customization)
11. [Altering Tables](#altering-tables)
12. [Deleting Data and Structures](#deleting-data-and-structures)

## Data Management

### Storage vs. Management
- Storing data is not the primary reason to use a database.
- Flat storage runs into issues like size, ease of updating, accuracy, security, and redundancy.

### Databases
- A database is an organized collection of related information that imposes rules on the contained data.
- Access to data is usually provided by a Database Management System (DBMS).

### RDBMS
- A Relational Database Management System (RDBMS) manages data through relations—collections of tables related by common fields.
- Examples include MS SQL Server, DB2, Oracle, and MySQL.

## Database Engine

### Database Engine Flow
- SQL Server uses the Client-Server Model.
  

### Top Database Engines
- Check [DB-Engines Ranking](http://db-engines.com/en/ranking) for the latest database engine rankings.

## Structured Query Language

- SQL is a programming language designed for managing data in a relational database.
- It includes four sections:
- **Data Definition**: Describes the structure of data.
- **Data Manipulation**: Stores and retrieves data.
- **Data Control**: Defines who can access the data.
- **Transaction Control**: Bundles operations and allows rollback.

## MySQL

- MySQL is an open-source RDBMS used in many large-scale websites like Google, Facebook, and YouTube.
- It works on multiple platforms, including macOS, Windows, and Linux.
- [Download MySQL Server](https://dev.mysql.com/downloads/mysql/)

## Table Relationships

- Splitting related data into different tables avoids redundancy.
- Relationships are created using Primary and Foreign Keys.

## Programmability

### Indices
- Indices make data lookup faster.
- **Clustered**: Bound to the primary key and physically sorts data.
- **Non-Clustered**: Can be any field and references the primary index.

### Views
- Views are prepared queries for displaying sections of data.

### Procedures, Functions, and Triggers
- **Procedures**: Carry out a predetermined action.
- **Functions**: Receive parameters and return a result.
- **Triggers**: Watch for database activity and react to it.

## Data Types in MySQL Server

### Numeric Data Types
- Numeric data types can be signed (negative and positive ranges) or unsigned (only positive).
- Examples include `INT`, `TINYINT`, `SMALLINT`, `MEDIUMINT`, `BIGINT`.

### String Types
- Character sets and collations define how strings are stored and compared.
- Examples: `CHAR`, `VARCHAR`, `TEXT`.

### Date Types
- Types include `DATE`, `TIME`, `DATETIME`, and `TIMESTAMP`.

## Database Modeling

### Working with IDEs
- We will manage databases with MySQL Workbench, enabling us to create and manage databases and tables easily.

### Creating a New Database
- Use the command: `CREATE DATABASE database_name;`

## Basic SQL Queries

### Create Table
- Example of creating a table:
```sql
CREATE TABLE people (
    id INT NOT NULL,
    email VARCHAR(50) NOT NULL,
    first_name VARCHAR(50),
    last_name VARCHAR(50)
);

