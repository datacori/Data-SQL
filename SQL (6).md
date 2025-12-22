# SQL Fundamentals Study (2025-12-22)

---

## Learning Goals
- Understand database security fundamentals  
- Learn how to manage users (create, modify, delete)  
- Understand roles and access control mechanisms

---

## Database Security
Database security refers to security mechanisms designed to prevent data and information leakage.  
Its main goal is to protect databases from unauthorized access, data loss, and misuse.

---

## Physical Security
Physical security protects databases from threats that can cause physical damage to the system.

Examples include:
- Protection against natural disasters
- Power failure prevention and backup systems
- Secure hardware environments with controlled access
- Restrictions on physical access to database equipment

---

## Security Through Authorization Management
Authorization management controls user access to the database through authentication and permission settings.

Key features:
- Login-based access control using ID and password
- Restricting user access to specific data or objects
- DBMS administrators (or authorized users) manage user creation, modification, and deletion

---

## Privilege Assignment
Privileges define what operations a user can perform on database objects.

Important points:
- Users can be granted privileges on all database objects
- `GRANT` command is used to assign privileges  
  (Privileges cannot be granted without specifying permissions)
- `WITH GRANT OPTION` allows users to grant their privileges to others

---

## Privilege Revocation
Privileges can be removed using the `REVOKE` command.

Syntax example:
```sql
REVOKE privilege ON object FROM user
CASCADE | RESTRICT;
```

CASCADE: Revokes privileges from the specified user and all users who received privileges from them

RESTRICT: Revokes privileges only if no dependent privileges exist

---

### Key 
- Database security includes both physical protection and logical acccess contro
- Authorization management ensures controlled and secure data access
- Privilege assignment and revocation are core components of SQL security management

---

## Role
A role is a collection of privileges on database objects.  
Roles are used to efficiently manage permissions in environments where multiple users access the database.

Key concepts:
- A role groups multiple privileges together
- Databases are often shared by many users, so role separation is necessary
- When role permissions change, all users assigned to that role are affected automatically  
  → No need to modify individual user privileges

---

## Creating a Role
A new role can be created using the following command:

```sql
GRANT role_name;
```

### Grant Privileges to a Role
Privileges can be assigned directly to a role instead of individual users
```sql
GRANT privilege ON object TO role_name;
```
This allows centralized privilede management

---

## Dropping a Role
If a role is no longer needed, it can be removed
```sql
DROP ROLE role_name;
```
---

## Assigning a Role to a User
Roles can be granted to users to apply all associated privileges at once
```sql
GRANT role_name TO user;
```
---

## Revoking a Role from a User
A role can be removed from a user if access is no longer required
```sql
REVOKE role_name FROM user;
```
---

### Key
- Roles simplify privilege management in multi-user database systems
- Changing a role updates permissions for all assigned users automatically
- Roles improve security, consistency, and administrative efficiency

---

## Key Learnings
- Database security concepts and access control management

---

## Reflections
- I have always been interested in cybersecurity, so studying database security was especially meaningful
- Even simple SQL commands should be clearly understood and interpreted
- At this stage, the theoretical concepts are still manageable and not overwhelming
- Keep going!

---

## Resources
- Practical SQL for Beginners: From MySQL Basics to Performance Optimization (Lecture Materials)

---

## Author
**RYU YEJIN**  

Data Analysis Learner  

Documenting SQL fundamentals from basics to practical database administration  

📧 Email: datacori00@gmail.com

Blog : https://blog.naver.com/datacori/224115728599

