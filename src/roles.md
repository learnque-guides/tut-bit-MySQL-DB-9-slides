# Roles

* Roles, introduced in MySQL 8.0, are collections of privileges.
* Roles are quite similar to users in how they are created, stored, and managed. To create a role, you need to execute:

```sql
CREATE ROLE [IF NOT EXISTS] role1[, role2[, role3 …]] 
```
* You can grant privileges to role:

```
GRANT SELECT ON database.* TO 'role_name';
```

* Role can be granted to user:

```sql
GRANT role [, role] TO 'user'@'%'
```

* Set role for user

```sql
SET ROLE 'role_name'
-- Or
ALTER USER 'bob'@'localhost' DEFAULT ROLE 'application_rw';
```

* You can revoke role with:

```sql
REVOKE role_name FROM 'user'@'%' 
```

* You can drop role with

```sql
DROP ROLE role_name;
```
