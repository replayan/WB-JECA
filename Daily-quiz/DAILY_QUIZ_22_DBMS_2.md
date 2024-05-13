# DBMS QUIZ

Date: May 13, 2024

**Source:** [Jecacracker](https://jecacracker.in/Daily_Quiz/)

---

## Multiple Choice Questions:

1. **Rho in relational algebra indicates_______.**
   - [ ] Selection
   - [ ] Projection
   - [x] Rename
   - [ ] Join
   - **Correct Answer:** Rename
   - **Explanation:** Rho in relational algebra is used to rename attributes or relations within a relational algebra expression.

2. **How can we select all rows where col is NULL?**
   - [x] `SELECT * FROM table WHERE col IS NULL;`
   - [ ] `SELECT * FROM table WHERE col = NULL;`
   - [ ] `SELECT * FROM table WHERE col == NULL;`
   - [ ] `SELECT * FROM table WHERE col = 0;`
   - **Correct Answer:** The correct SQL statement to select all rows where a column (let's call it "col") is NULL is:

   ```sql
   SELECT * FROM table WHERE col IS NULL;
   ```

   The `IS NULL` operator is used to check if a column contains a NULL value. So, the correct option is the first one.
   - **Explanation:** In SQL, the correct way to check for NULL values is using the `IS NULL` operator.

3. **Which form simplifies and ensures that there are minimal data aggregates and repetitive groups?**
   - [ ] 1NF
   - [ ] 2NF
   - [x] 3NF
   - [ ] All of the mentioned
   - **Correct Answer:** 3NF
   - **Explanation:** Third Normal Form (3NF) ensures minimal data aggregates and repetitive groups by eliminating transitive dependencies.

4. **NATURAL JOIN can also be termed as_______.**
   - [ ] Combination of Union and cartesian product
   - [ ] Combination of Selection and cartesian product
   - [x] Combination of Projection and cartesian product
   - [ ] None
   - **Correct Answer:** Combination of Projection and cartesian product
   - **Explanation:** NATURAL JOIN combines tuples based on equality of values in attributes, similar to a combination of Projection and cartesian product.

5. **An embedded pointer provides_______.**
   - [ ] Physical record key
   - [ ] An inserted index
   - [x] A secondary access path
   - [ ] All of these
   - **Correct Answer:** A secondary access path
   - **Explanation:** An embedded pointer in database systems typically provides a secondary access path, often used for implementing secondary indexes.
