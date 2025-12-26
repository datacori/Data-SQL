# SQL Fundamentals Study (2025-12-24)

## Learning Goals

This section focuses on understanding the concept of **Entity** in database design.

- Definition of an Entity
- Characteristics of an Entity
- Types and classification of Entities
- Attributes, classification, and naming conventions

---

## Entity

An **Entity** is a logically identifiable unit that represents information required for business operations and data management.

### Key Characteristics
- Represents a real-world object or concept that needs to be stored and managed
- Can exist conceptually even before being implemented in a database
- Serves as the foundation for database table design

### Entity Type and Entity Set
- **Entity Type**: A category that defines a group of entities with the same attributes
- **Entity Set**: A collection of entities belonging to the same entity type

### Examples of Entities
- People (e.g., customers, employees)
- Places (e.g., cities, locations)
- Objects (e.g., products, items)
- Concepts or events that require data storage

In relational databases, **entities are typically implemented as tables**.

---

## Entity Classification Examples

- *Apple* → Company  
- *Seoul* → Location  
- *James* → Person  
- *Amazon* → Organization  

These examples illustrate how individual entities belong to specific entity types.

---

## Key Takeaways

- Entities represent core objects or concepts in database design
- Clear entity definition is essential for effective data modeling
- Entity types help organize and standardize database structures

---

## Entity Type Characteristics

An **Entity Type** defines a group of entities that share the same structure and attributes within a database system.

### Key Characteristics
- Must represent information that is essential and must be managed within the system
- Each entity instance can be uniquely identified
- Exists conceptually as a collection of related entities
- Actively used in business processes and workflows
- Must include at least one **attribute**
- Must participate in at least one relationship with another entity type

---

## Components of an Entity Type

### Categories
Entity types can represent different categories such as:
- Company
- Location
- Person

### Common Attributes
Attributes shared across entities within the same entity type, for example:
- Name
- Country
- Founded Date

### Subtypes
Entity types may include subtypes that inherit attributes from the parent entity type:
- Tech Company
- Retail Company
- Media Company

---

## Key Takeaways

- Entity types define the structure of database tables
- Attributes and relationships are mandatory components of entity types
- Subtypes enable flexible and scalable data modeling

---

