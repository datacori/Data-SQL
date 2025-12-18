# SQL fundamentals study (2025-12-18)
---
## Learning goals

### Database Types and Characteristics

- Hierarchical Database
- Network Database
- Key-Value Database
- Relational Database
- Types of NoSQL Databases

---

## Hierarchical Database

A hierarchical database organizes data in a **tree-like structure**, where records are connected through **parent-child relationships**.

### Key Characteristics
- Data is structured as a tree
- Represents repetitive parent–child relationships
- Each parent record can have **multiple child records**
- Each child record has **only one parent record**

### Structure Overview
- **Root Record**: The top-level record in the hierarchy
- **Parent Record**: A record that owns one or more child records
- **Child Record**: A record that belongs to exactly one parent



This structure is efficient for representing **one-to-many relationships**, but it lacks flexibility when handling many-to-many relationships.
