# DBMS QUIZ

Date: May 03, 2024

**Source:** [Jecacracker](https://jecacracker.in/Daily_Quiz/)

---

1. **What is the default sorting order of ORDER BY clause?**

   - [X] ascending
   - [ ] descending
   - [ ] no default sorting order is there
   - [ ] None of the above

   **Correct Answer: ascending**

   **Explanation:** The default sorting order of the ORDER BY clause in SQL is ascending. If no specific order (ASC or DESC) is provided after the column names in the ORDER BY clause, the database engine will sort the results in ascending order by default.

2. **How can we select all rows where col is NULL?**

   - [x] SELECT * FROM table WHERE col IS NULL;
   - [ ] SELECT * FROM table WHERE col = NULL;
   - [ ] SELECT * FROM table WHERE col == NULL;
   - [ ] SELECT * FROM table WHERE col = 0;

   **Correct Answer: SELECT * FROM table WHERE col IS NULL;**

   **Explanation:** In SQL, to select all rows where a column "col" is NULL, you use the IS NULL comparison operator.

3. **Relational Algebra is ______ query language.**

   - [x] Non-procedural
   - [ ] Schema
   - [ ] Singleton
   - [ ] Procedural

   **Correct Answer: Non-procedural**

   **Explanation:** Relational Algebra is a non-procedural query language. It provides a theoretical foundation for relational databases and is used to define queries without specifying how to do it.

4. **Rows of a relation are known as _____.**

   - [ ] Degree
   - [ ] Entity
   - [x] Tuple
   - [ ] Attribute

   **Correct Answer: Tuple**

   **Explanation:** Rows of a relation are known as "Tuples." Each tuple represents a single record or row in the relation, containing a collection of attribute values.

5. **What is a table joined with itself called?**

   - [ ] Join
   - [x] Self Join
   - [ ] Equi Join
   - [ ] Outer Join

   **Correct Answer: Self Join**

   **Explanation:** A table joined with itself is called a "Self Join." In a self join, a table is joined with itself based on a related column within the same table.
