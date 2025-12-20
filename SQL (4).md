# SQL Fundamentals study (2025-12-20)
---

## Learning Goals 
- Relational Algebra
- Relational Operations: Selection, Projection, Join, Division
- Set Operations: Union, Intersection, Difference, Cartesian Product

---

## Relational Algebra
- A formal query language that uses **mathematical operations** to retrieve desired results from relations
- Describes **how** to obtain a result relation by applying operations to one or more relations
- Procedural in nature: each step defines how the result is produced

---

## Purpose of Relational Algebra
- Provides a theoretical foundation for querying relational databases
- Allows step-by-step execution of operations on relations to produce a result relation
- Helps understand how queries are processed internally in a DBMS

---

## Relationship with SQL and DBMS
- SQL is based on **relational calculus**, but internally optimized using **relational algebra**
- DBMS query execution engines rely on relational algebra to process SQL queries efficiently

---

## Relational Algebra Operators

Relational algebra operators are classified into two main categories:

### 1. Basic Relational Operations
- Selection
- Projection
- Join
- Division
- Renaming

### 2. Set Operations
- Union
- Intersection
- Difference
- Cartesian Product

---

## Selection (σ)

- An operation used to **extract specific tuples (rows)** from a relation
- A **unary operation** that operates on a single relation
- Returns tuples that **satisfy a given condition**
- The **degree (number of attributes)** of the result relation remains the same as the original relation
- The **cardinality (number of tuples)** of the result relation is **less than or equal to** that of the original relation

### Characteristics
- Filters rows based on conditions
- Does not change the schema of the relation
- Corresponds to the `WHERE` clause in SQL

---

## Projection (π)

- An operation used to **extract specific attributes (columns)** from a relation
- A **unary operation** that operates on a single relation
- The **degree (number of attributes)** of the result relation is **less than or equal to** that of the original relation
- The **cardinality (number of tuples)** remains the same, but **duplicate tuples are removed**

### Notation
- π<sub>attributes</sub>(R)

### Characteristics
- Selects columns rather than rows
- Does not change the number of tuples (except for duplicate elimination)
- Corresponds to the `SELECT` clause in SQL

---

## Join (⨝)

- An operation that **combines tuples from two relations** based on **common attribute values**
- The join condition requires attributes from both relations to share the **same domain**
- Conceptually equivalent to performing a **Cartesian product followed by a selection**

### Notation
- R ⨝<sub>condition</sub> S  
- R ⨝ S = σ<sub>condition</sub>(R × S)

### Types of Join Operations

#### Basic Join
- Compares attribute values between two relations
- Returns tuples that satisfy the join condition

#### Extended Join
- Returns the combined tuples after joining two relations

### Result Characteristics
- Only tuples with **matching values on common attributes** are included
- Used to represent relationships between relations (tables)

### SQL Mapping
- Corresponds to `JOIN ... ON` or `WHERE` clause joins in SQL

---

## Division (÷)

- An operation performed on **sets of attribute values** in relations
- Used to find tuples that are **associated with all values** in another relation
- Commonly applied when a query requires a **“for all” condition**

### Characteristics
- Useful for queries such as “find entities related to all specified items”
- More complex than other relational algebra operations
- Often implemented in SQL using subqueries or `GROUP BY` with `HAVING`

---

## Set Operations

Set operations combine relations based on set theory principles.  
All participating relations must have:
- The **same number of attributes**
- The **same attribute order**
- Compatible **domains**

---

### Union (∪)

- Combines tuples from **two relations into a single relation**
- Duplicate tuples are automatically removed
- The resulting relation uses the **attribute names of the first relation**

### Characteristics
- Requires union compatibility between relations
- Corresponds to the `UNION` operator in SQL

---

### Intersection (∩)

- Returns tuples that are **common to both relations**
- Both relations must have:
  - The same attribute order
  - Compatible domains
- The resulting relation uses the **attribute names of the first relation**

### Characteristics
- Only tuples that exist in **both relations** are included
- Corresponds to the `INTERSECT` operator in SQL

---

### Set Difference (−)

- Returns tuples that **exist in the first relation but not in the second**
- Both relations must have:
  - The same attribute order
  - Compatible domains
- The resulting relation uses the **attribute names of the first relation**

### Characteristics
- Useful for excluding specific tuples from a result set
- Corresponds to the `EXCEPT` or `MINUS` operator in SQL

---

### Cartesian Product (×)

- Conceptually equivalent to the **mathematical Cartesian product**
- Combines every tuple of the first relation with **every tuple of the second relation**
- Produces a single relation containing all possible tuple combinations
- The resulting relation places attributes of the **first relation first**, followed by those of the second relation
- Unlike other set operations, **attribute order and domain compatibility are not required**

### Characteristics
- Often used as the basis for join operations
- Can generate very large result sets
- Typically followed by a selection condition to form meaningful joins

---

## Key Learnings
- Relational Algebra
- Relational Operations
- Set Operations

---

## Reflections
- Although mathematics is not my strongest area, learning relational algebra was manageable
- Prior experience studying PSAT helped me understand set concepts more easily
- I realized the importance of starting from fundamental concepts and building up step by step
- Keep going!

---

## Resources
- Practical SQL Course: From MySQL Basics to Query Writing and Performance Optimization (Lecture Materials)

---

## Author

**RYU YEJIN**  

Data Analysis Learning Log 

From SQL fundamentals to real-world projects  

📧 Email: datacori00@gmail.com

Blog :
