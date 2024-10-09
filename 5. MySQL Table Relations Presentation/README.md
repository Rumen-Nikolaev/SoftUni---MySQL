# Database Design and Table Relations

## Table of Contents
1. [Database Design](#database-design)
2. [Table Relations](#table-relations)
3. [JOINs](#joins)
4. [Cascade Operations](#cascade-operations)
5. [E/R Diagrams](#er-diagrams)

## Database Design
### Fundamental Concepts
Steps in Database Design:
1. Identification of the entities
2. Defining table columns
3. Defining primary keys
4. Modeling relationships
5. Defining constraints
6. Filling test data

### Identification of Entities
- Entity tables represent objects from the real world.
- Most often, they are nouns in the specification.
- **Example**: We need to develop a system that stores information about students trained in various courses held in different towns. When registering a new student, the following information is entered: name, faculty number, photo, and date.
- **Entities**: Student, Course, Town

### Identification of the Columns
- Columns clarify the entities in the specification text.
- **Example**: Students have the following characteristics: Name, faculty number, photo, date of enlistment, and a list of courses they visit.

### How to Choose a Primary Key?
- Always define an additional column for the primary key.
- Don't use an existing column (e.g., SSN).
- It can be an integer number.
- Must be declared as a PRIMARY KEY.
- Use `AUTO_INCREMENT` to implement auto-increment.
- Put the primary key as the first column.

### Identification of Relationships
- Relationships are dependencies between the entities.
- **Example**:
  - "Students are trained in courses" – many-to-many relationship.
  - "Courses are held in towns" – many-to-one (or many-to-many) relationship.

## Table Relations
### Relationships
- Relationships between tables are based on interconnections: PRIMARY KEY / FOREIGN KEY.

#### Primary Key and Foreign Key Example
- **Towns Table**:




### Types of Relationships
- **One-to-Many**: e.g., mountains / peaks
- **Many-to-Many**: e.g., student / course
- **One-to-One**: e.g., driver / car

## JOINs
- Table relations are useful when combined with JOINS.
- JOINS allow retrieval of data from two tables simultaneously.
- **Example**:
```sql
SELECT * FROM table_a
JOIN table_b ON table_b.common_column = table_a.common_column;

