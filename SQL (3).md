# SQL Fundamentals study (2025-12-19)
---

## Learning Goals
- Understand the Relational Data Model
- Learn the concepts of relations, schemas, and instances
- Identify different types of relational keys
- Understand integrity constraints

---

## Relational Data Model

### Overview
The **Relational Data Model** is designed based on mathematical **set theory**.  
It represents data in a structured and logical way, making it easier to store, retrieve, and manage data using SQL.

SQL, which is based on the relational model, allows users to express desired data in a **non-procedural (declarative)** manner.

---

### Core Concepts

#### Relations
- Data is represented as **relations**, which are two-dimensional tables
- Each relation consists of rows (tuples) and columns (attributes)

#### Schema and Instance
- **Schema**: Defines the structure of a relation (table name, attributes, data types)
- **Instance**: The actual data stored in the relation at a specific point in time

---

### Relational Model Components
- **Relations**: Tables that store data
- **Integrity Constraints**: Rules that data must satisfy
- **Relational Operations**: Operations used to retrieve and manipulate data
- **Relational Calculus**: A theoretical foundation for query formulation

---

### Integrity Constraints
Integrity constraints define conditions that the data stored in a relation must satisfy.  
They ensure data accuracy, consistency, and reliability within a database.

---

## Key Takeaways
- The relational data model organizes data into structured tables
- SQL is built upon the principles of the relational model
- Schemas define structure, while instances represent actual data
- Integrity constraints play a crucial role in maintaining data consistency

---

## Relation

### Overview
A **relation** is a table composed of rows and columns in the relational data model.  
In practice, a relation corresponds directly to a **table** in a database.

Each relation represents a relationship among data and is stored in a two-dimensional structure.

---

### Characteristics of a Relation
- A relation is represented as a table with rows and columns
- The order of attributes (columns) does **not** matter
- The order of tuples (rows) does **not** matter
- Duplicate tuples are **not allowed** in a relation

---

### Relation vs Table
- **Relation**: A theoretical concept in the relational data model
- **Table**: The physical implementation of a relation in a database system

---

### Example
In the relational data model, entities such as **Customers** and **Orders** are stored in separate relations.  
These relations can be linked through common attributes (e.g., `Customer_ID`).

This structure allows data to be:
- Stored efficiently
- Queried flexibly
- Maintained with integrity

---

### Key Takeaways
- Relations are the foundation of the relational data model
- They store data in a structured, two-dimensional format
- Data order does not affect the meaning of a relation

---

## Relation Schema

### Overview
A **relation schema** defines the basic structure of a relation in a relational database.  
It describes how the relation is organized and what kind of information it contains.

---

### Components of a Relation Schema

- **Header**  
  The first row of a relation that describes the characteristics of the data

- **Attribute**  
  Each column in a relation, where every attribute has a unique name

- **Domain**  
  Defines the set of valid values that an attribute can have

- **Degree**  
  Indicates the number of attributes in a relation

---

### Key Takeaways
- The schema defines the structure, not the actual data
- Attributes and domains ensure data consistency
- Degree represents how many attributes a relation contains

---

## Relation Instance

### Overview
A **relation instance** is the actual set of data stored in a relation schema at a specific moment in time.  
It represents the current contents of the table.

---

### Components of a Relation Instance

- **Tuple**  
  Each row in a relation instance

- **Cardinality**  
  The number of tuples stored in a relation

---

### Constraints on Relation Instances
- All tuples in a relation must be unique
- Duplicate tuples are not allowed

---

### Key Takeaways
- The instance represents real data, while the schema represents structure
- Cardinality changes as data is inserted or deleted
- Instances must follow the rules defined by the schema

---

## Types of Relational Keys

### Key
A **key** is an attribute or a set of attributes used to **uniquely identify a tuple** in a relation.

---

### Super Key
A **super key** is a set of one or more attributes that can uniquely identify a tuple.
- It may contain unnecessary (non-minimal) attributes

---

### Candidate Key
A **candidate key** is a **minimal super key**.
- It uniquely identifies tuples
- No attribute can be removed without losing uniqueness
- A relation may have multiple candidate keys

---

### Primary Key
A **primary key** is a candidate key selected to uniquely identify tuples in a relation.
- Only one primary key can exist per relation
- Must contain **unique** values
- **NULL values are not allowed**
- The value of a primary key should not change

---

### Alternate Key
An **alternate key** is a candidate key that is **not chosen** as the primary key.

---

### Foreign Key
A **foreign key** is an attribute that references the **primary key of another relation**.
- It represents relationships between relations
- The referenced and referencing attributes must have the same domain
- When the referenced primary key value changes, the foreign key value must also change
- A foreign key can reference the same relation (self-referencing)

---

### Key Takeaways
- Keys ensure entity integrity and data uniqueness
- Candidate keys are minimal identifiers
- Primary and foreign keys are essential for relational integrity

---

## Integrity Constraints

### Overview
**Data integrity** ensures the accuracy, consistency, and reliability of data stored in a database.  
Integrity constraints define rules that data must follow to maintain high data quality.

---

### Types of Integrity Constraints
- **Domain Integrity**
- **Entity Integrity**
- **Referential Integrity**

These constraints help prevent invalid, inconsistent, or meaningless data from being stored.

---

### Domain Integrity Constraint
Domain integrity restricts the values that an attribute can take.
Only values defined within the attribute’s domain are allowed.

Common domain constraints include:
- Data type
- `NOT NULL`
- `DEFAULT`
- `CHECK`

---

### Entity Integrity Constraint
Entity integrity ensures that each tuple in a relation can be uniquely identified.
- The **primary key must be unique**
- **NULL values are not allowed** in the primary key

This guarantees that every record represents a distinct entity.

---

### Referential Integrity Constraint
Referential integrity maintains consistency between related relations.
- A foreign key must reference an existing primary key
- Referenced and referencing attributes must have the same domain
- Changes in the parent relation affect the child relation

This constraint ensures valid relationships between tables.

---

### Key Takeaways
- Integrity constraints protect data accuracy and consistency
- Domain integrity controls valid attribute values
- Entity integrity guarantees unique entity identification
- Referential integrity maintains valid relationships between relations

---

## Key Learnings
- Gained a solid understanding of the relational data model
- Learned different types of relational keys and their roles
- Understood various integrity constraints and their importance

---

## Reflections
- Although the content is theoretical, it did not feel overwhelming
- Connecting SQL concepts with previously learned Python terminology made learning easier
- Stay consistent and keep going 🚀

---

## Resources
- Introduction to MySQL: From Basics to Query Writing and Performance Optimization (Course Materials)

---

## Author

**RYU YEJIN**  

Aspiring Data Analyst 

SQL Learning Journey from Fundamentals to Practice  

📧 Email: datacori00@gmail.com

Blog : https://blog.naver.com/datacori/224114179433
