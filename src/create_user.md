# Create, modify, delete user

A new user can be created with:

```sql
CREATE USER 'test'@'localhost' IDENTIFIED BY '<secret>';
SELECT plugin FROM mysql.user WHERE
    user = 'test' AND host = 'localhost'; 
```

More complex example:

```sql
CREATE USER 'bob'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password'
DEFAULT ROLE 'user_role'
REQUIRE SSL
AND CIPHER 'EDH-RSA-DES-CBC3-SHA'
WITH MAX_USER_CONNECTIONS 10
PASSWORD EXPIRE NEVER;
```

We can use ALTER statement for modifying user;

```sql
ALTER USER 'bob'@'localhost' IDENTIFIED WITH mysql_native_password BY 'new_password';
ALTER USER 'bob'@'localhost' ACCOUNT LOCK;
ALTER USER 'bob'@'localhost' ACCOUNT UNLOCK;
```

User can be removed with:

```sql
DROP USER 'bob'@'localhost';
```