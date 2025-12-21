# SQL Fundamentals study (2025-12-21)
---

# SQL Transaction Basics

## Learning Goals
- Understand the concept of transactions
- Learn transaction properties (Atomicity, Consistency, Isolation, Durability)
- Understand the relationship between transactions and DBMS
- Learn concurrency control
- Understand database locks

---

## Transaction

A **transaction** is a logical unit of work in a DBMS that consists of one or more SQL statements.

### Key Characteristics
- A transaction is treated as a **single logical operation**
- It follows the **all-or-nothing** principle
- If a failure occurs, the database can be restored to its previous state
- It helps separate tasks when multiple operations access the same data concurrently

### Transaction Control Statements
```sql
BEGIN TRANSACTION;  -- Start
COMMIT;             -- End (save changes)
ROLLBACK;           -- Undo changes
```
---

## Transaction Properties (ACID)

Transactions in a DBMS follow four fundamental properties known as **ACID** to ensure reliability and integrity.

---

### 1. Atomicity
Atomicity means that a transaction must be treated as a **single indivisible unit**.

- Either **all operations are executed**, or **none are executed**
- Partial execution is not allowed
- Transaction control statements:
  ```sql
  BEGIN TRANSACTION;
  COMMIT;
  ROLLBACK;
```
- If an error occurs during executuion, the DBMS users recovery algorithms to cancel changes
- rollback explicitily cancels the current transaction

```

## Consistency
Consistency ensures that a transaction brings the database from one valid state to another

- All integrity constraints must be satisfied
- Enforced through : create table / alter table constraints
- Data remains logically correct before and after the transaction

---
## Isolation
Isolation ensures that concurrently executing transactions do not interfere with each other

- Transactions are executed independently
- Intermediate states of a transaction are not visible to others
- To maintain isolation:

Temporary changes must be protected

Other transactions must be prevented from accessing uncommitted data
- Requires concurrency control mechanisms such as locking

---

## Durability
Duraility guarantees that once a transaction is successfully committed, the result is permanently stored

- Committed data is recorded in the database
- Data is preserved even in case of system failure or crash
- DBMS is responsible for ensuring persistence

---

## Transactions and DBMS

A **DBMS (Database Management System)** provides built-in mechanisms to support and guarantee transaction properties.

---

### Role of DBMS in Transaction Management

- The DBMS ensures that transactions satisfy the **ACID properties**:
  - Atomicity
  - Consistency
  - Isolation
  - Durability

- To maintain **consistency**, the DBMS enforces:
  - Integrity constraints (domain constraints, key constraints, referential constraints)

- To maintain **isolation** in concurrent environments:
  - The DBMS uses concurrency control algorithms
  - Prevents conflicts between simultaneous transactions

---

### Mapping Transaction Properties to DBMS Functions

| Transaction Property | DBMS Support Function |
|----------------------|-----------------------|
| Atomicity | Logging, Rollback, Recovery |
| Consistency | Integrity Constraints |
| Isolation | Concurrency Control |
| Durability | Backup and Recovery |

---

## Concurrency Control

**Concurrency Control** is a mechanism used by the DBMS to manage simultaneous execution of transactions while preserving data consistency and correctness.

---

### Purpose of Concurrency Control

- Prevents violations of **consistency**
- Ensures that concurrent transactions do not interfere with each other
- Allows multiple transactions to be executed efficiently at the same time

---

### Key Characteristics

- Transactions executed concurrently should not be aware that other transactions are accessing the same data
- The final result must be equivalent to some **serial execution** of transactions

---

### Lost Update Problem

The **Lost Update Problem** occurs when:

- Two or more transactions update the same data concurrently
- One transaction’s update overwrites another’s update
- As a result, one update is lost

⚠️ In a properly designed DBMS, this situation **must never occur**

---

### Why Concurrency Control Is Necessary

- Improves system performance by allowing parallel execution
- Prevents data anomalies caused by simultaneous access
- Maintains database reliability in multi-user environments

---

### Summary

- Concurrency control protects data consistency during simultaneous transactions
- Without concurrency control, data integrity cannot be guaranteed

---

### Key DBMS Functions for Transactions

- **Log Management**
  - Records transaction changes for recovery

- **Integrity Constraint Enforcement**
  - Ensures data validity and consistency

- **Concurrency Control**
  - Controls simultaneous access to shared data

- **Backup and Recovery**
  - Restores data after system failures

---

### Summary
- Transactions define *what* properties must be guaranteed
- The DBMS provides *how* those properties are enforced
- Transaction reliability depends directly on DBMS internal mechanisms

---

## Lock

A **Lock** is a mechanism used by a DBMS to control access to data when a transaction reads or modifies it.

Locks are essential for **concurrency control** and are used to prevent problems such as **lost updates**.

---

### Purpose of Locks

- Prevents data inconsistency during concurrent access
- Ensures safe execution of multiple transactions
- Resolves concurrency anomalies caused by simultaneous updates

---

### Types of Locks

#### Shared Lock (S Lock)

- Used when a transaction **reads** data
- Multiple transactions can hold a shared lock on the same data
- Does **not** allow write operations

#### Exclusive Lock (X Lock)

- Used when a transaction **reads and writes** data
- Only one transaction can hold an exclusive lock on the data
- Blocks both read and write access by other transactions

---

### Lock Rules

- If no lock exists on a data item, a transaction can request a lock
- If a transaction cannot obtain the required lock, it must **wait**
- Locks are released after the transaction completes

---

### Lock Request Rules

- To **read** data item `X` → request **Shared Lock (S Lock)**
- To **read and write** data item `X` → request **Exclusive Lock (X Lock)**

---

### Lock Compatibility

| Existing Lock | Request S Lock | Request X Lock |
|--------------|---------------|---------------|
| S Lock       | Allowed       | Not Allowed   |
| X Lock       | Not Allowed   | Not Allowed   |

---

### Summary

- Locks are fundamental to transaction isolation
- Shared locks allow concurrent reads
- Exclusive locks ensure safe updates
- Proper lock management prevents lost updates and maintains data integrity

---

## Key Learnings

- Transaction concepts and ACID properties, and their relationship with DBMS
- Concurrency control and the lost update problem
- Lock types and lock rules

---

## Reflections

- Transactions represent the logical unit of work used by a DBMS to handle data safely
- Although I am still learning the theory, organizing it in Markdown helped reinforce my understanding
- Writing technical concepts in English made the material more challenging but also more valuable
- Keep going!

---

## Resources

- 입문자·실무자 누구나 실리콘밸리 엔지니어의 감성으로 시작하는 MySQL
  (From basic queries to performance optimization) – lecture materials

---

## Author

**RYU YEJIN**  

Data Analysis Learning Log

From SQL fundamentals to real-world projects  

Email: datacori00@gmail.com

Blog : 
