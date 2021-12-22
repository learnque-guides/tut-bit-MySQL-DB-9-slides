# Users, DCL

* Users in MySQL are special objects used for the purpose of:
  * Authentication (making sure that a user can access the MySQL server)
  * Authorization (making sure that a user can interact with objects in the database)
* One thing that makes MySQL distinct from other DBMSs is that users do not own schema objects.
* Users in MySQL are also a bit different than in other databases, because the user object includes a network access control list (ACL)
* MySQL stores all information related to users and privileges in special tables in the mysql system database called grant tables.

```sql
SELECT * FROM mysql.user WHERE user = 'root';
```

We do not need to edit grant tables directly. Instead we use DCL.