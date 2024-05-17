# Database Management System (DBMS)

## 1. Introduction to Databases
### Definition
A **Database Management System (DBMS)** is a software system that uses a standard method of cataloging, retrieving, and running queries on data.

### Key Concepts
- **Data**: Raw facts and figures.
- **Information**: Processed data.
- **Database**: Organized collection of data.
- **DBMS**: Software to manage databases.

### Advantages of DBMS
- **Data Redundancy Control**: Minimizes duplication.
- **Data Integrity**: Ensures accuracy and consistency.
- **Data Security**: Protects data from unauthorized access.
- **Data Independence**: Separates data and application.
- **Efficient Data Access**: Optimizes query processing.

### Types of Databases
- **Hierarchical Database**
- **Network Database**
- **Relational Database**
- **Object-Oriented Database**

---

## 2. ER Diagram (Entity-Relationship Diagram)
### Definition
An **ER Diagram** is a visual representation of entities and their relationships.

### Components
- **Entity**: An object that exists (e.g., Student, Course).
- **Attribute**: Properties of entities (e.g., Student Name, Course ID).
- **Relationship**: Link between entities (e.g., Enrols in).

### Symbols
- **Rectangle**: Entity
- **Ellipse**: Attribute
- **Diamond**: Relationship
- **Line**: Link between entities and relationships

### Cardinality
Defines the number of instances of one entity that can be associated with an instance of another entity.
- **One-to-One (1:1)**
- **One-to-Many (1:M)**
- **Many-to-Many (M:N)**

---

## 3. Relational Algebra
### Definition
**Relational Algebra** is a procedural query language that works on relational databases.

### Basic Operations
- **Select (σ)**: Selects rows based on a condition.
- **Project (π)**: Selects columns.
- **Union (∪)**: Combines results of two queries.
- **Set Difference (-)**: Returns rows in one query but not the other.
- **Cartesian Product (×)**: Combines all rows of two tables.
- **Rename (ρ)**: Renames the output relation.

### Example
```sql
σ (age > 25) (Employee)
π (name, salary) (Employee)
```

---

## 4. Relational Calculus
### Definition
**Relational Calculus** is a non-procedural query language.

### Types
- **Tuple Relational Calculus (TRC)**
  - Uses tuple variables.
  - Example: `{t | t ∈ Employee AND t.age > 25}`

- **Domain Relational Calculus (DRC)**
  - Uses domain variables.
  - Example: `{<name, age> | ∃ t ∈ Employee (t.name = name AND t.age = age AND age > 25)}`

---

## 5. SQL (Structured Query Language)
### Definition
**SQL** is a standard language for accessing and manipulating databases.

### Categories
- **DDL (Data Definition Language)**: `CREATE`, `ALTER`, `DROP`
- **DML (Data Manipulation Language)**: `SELECT`, `INSERT`, `UPDATE`, `DELETE`
- **DCL (Data Control Language)**: `GRANT`, `REVOKE`
- **TCL (Transaction Control Language)**: `COMMIT`, `ROLLBACK`, `SAVEPOINT`

### Basic Queries
```sql
-- Create a table
CREATE TABLE Student (
    ID INT PRIMARY KEY,
    Name VARCHAR(100),
    Age INT
);

-- Insert data
INSERT INTO Student (ID, Name, Age) VALUES (1, 'John Doe', 22);

-- Select data
SELECT * FROM Student;

-- Update data
UPDATE Student SET Age = 23 WHERE ID = 1;

-- Delete data
DELETE FROM Student WHERE ID = 1;
```

---

## 6. Normalization
### Definition
**Normalization** is the process of organizing data to minimize redundancy.

### Normal Forms
- **1NF (First Normal Form)**: Eliminate duplicate columns.
- **2NF (Second Normal Form)**: Eliminate subsets of data that apply to multiple rows.
- **3NF (Third Normal Form)**: Eliminate columns not dependent on primary key.
- **BCNF (Boyce-Codd Normal Form)**: A stronger version of 3NF.

### Example
A table is in 1NF if it has only atomic (indivisible) values.

---

## 7. Transactions
### Definition
A **Transaction** is a sequence of operations performed as a single logical unit of work.

### Properties (ACID)
- **Atomicity**: All operations are completed or none are.
- **Consistency**: Ensures database is consistent before and after the transaction.
- **Isolation**: Transactions are isolated from each other.
- **Durability**: Results are permanent after transaction completion.

### Example
```sql
BEGIN TRANSACTION;
UPDATE Account SET Balance = Balance - 100 WHERE AccountID = 1;
UPDATE Account SET Balance = Balance + 100 WHERE AccountID = 2;
COMMIT;
```

---

## 8. Indexing
### Definition
**Indexing** improves the speed of data retrieval operations on a database table.

### Types
- **Primary Index**: Automatically created with the primary key.
- **Secondary Index**: Created manually for faster search.
- **Clustered Index**: Alters the physical order of the table.
- **Non-Clustered Index**: Does not alter physical order, uses a separate structure.

### Example
```sql
CREATE INDEX idx_name ON Student (Name);
```

---

## 9. Query Optimization
### Definition
**Query Optimization** refers to the process of improving the efficiency of query execution.

### Techniques
- **Use of Indexes**: Helps in faster data retrieval.
- **Query Rewriting**: Simplifying the query structure.
- **Cost-Based Optimization**: Uses cost estimates to choose the best execution plan.
- **Join Algorithms**: Choosing the optimal way to perform joins (Nested Loop, Hash Join, etc.).

### Example
Instead of:
```sql
SELECT * FROM Employee WHERE department = 'HR' AND salary > 50000;
```
Use:
```sql
SELECT * FROM Employee WHERE salary > 50000 AND department = 'HR';
```
