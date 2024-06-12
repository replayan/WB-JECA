# Database Management Systems (DBMS) QUIZ

Date: June 12, 2024

**Source:** [Jecacracker](https://jecacracker.in/Daily_Quiz/)

---

## Multiple Choice Questions:

**1. In an E-R diagram, multivalued attributes are represented by:**

* A. Rectangle
* B. Dashed ellipse **(Correct Answer)**
* C. Double ellipse
* D. Diamond

* Explanation:
    * Rectangle represents entities.
    * Dashed ellipse represents derived attributes.
    * Diamond represents relationships.
    * Double ellipse is specifically used for multivalued attributes.

**2. Which of the following is not an example of DBMS?**

* A. MySQL
* B. Microsoft Access
* C. IBM DB2
* D. Google **(Correct Answer)**

* Explanation:
    * MySQL, Microsoft Access, and IBM DB2 are all popular Database Management Systems.
    * Google is a search engine and cloud computing company. While it uses various DBMS products internally, it doesn't itself function as a general-purpose DBMS for users.

**3. Which of the following is the property of transaction that protects data from system failure?**

* A. Atomicity
* B. Isolation
* C. Durability **(Correct Answer)**
* D. Consistency

* Explanation:
    * Durability ensures that once a transaction is successful, the data changes are permanently stored on disk and persist even if a system failure occurs.
    * Atomicity ensures all operations within a transaction are completed or none are (preventing partial updates).
    * Isolation ensures concurrent transactions don't interfere with each other's data.
    * Consistency ensures the data remains valid after a transaction.

**4. To remove a relation from an SQL database, we use the ______ command.**

* A. Delete
* B. Purge
* C. Remove
* D. Drop table **(Correct Answer)**

* Explanation:
    * Delete is used to remove specific rows from a table based on a condition.
    * Purge and Remove aren't standard SQL commands for table deletion.
    * Drop table is the specific command for this purpose.

**5. The attribute AGE is calculated from DATE_OF_ BIRTH. The attribute AGE is**

* A. Single valued
* B. Multi valued
* C. Composite
* D. Derived **(Correct Answer)**

* Explanation:
    * Single-valued attributes have one value per entity (e.g., name, ID). AGE isn't multi-valued (multiple ages).
    * Composite attributes are formed by combining other attributes (e.g., full address). AGE isn't a combination.
    * Derived attributes are calculated from other stored attributes. Since AGE is based on DATE_OF_BIRTH, it's derived.
