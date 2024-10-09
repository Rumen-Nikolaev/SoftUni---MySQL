# Built-in Functions in MySQL Server

## SoftUni Team
Technical Trainers
Software University

## Table of Contents
1. [Functions in MySQL](#functions-in-mysql)
2. [String Functions](#string-functions)
3. [Math Functions](#math-functions)
4. [Date Functions](#date-functions)
5. [Wildcards](#wildcards)
6. [Questions](#questions)

## Functions in MySQL

MySQL functions are categorized as follows:
- **String Functions**: For manipulating text, both from table values or user input (e.g., concatenate column values).
- **Math Functions**: For calculations and working with aggregate data (e.g., perform geometry and currency operations).
- **Date and Time Functions**: For finding the length of timespan.
- **Other Functions**: Various other built-in functions.

## String Functions

### String Functions (1)
- **SUBSTRING()**: Extracts part of a string.
  ```sql
  SUBSTRING(String, Position)
  SUBSTRING(String, Position, Length)
  SUBSTRING(String FROM Position FOR Length)


