# Privileges

To use existing privileges you can use:

```sql
SHOW PRIVILEGES;
```

User `root` have *super* privilege that let's for him to do anything.

## Privilege Management Commands

We are using *GRANT* statement to give a privilege to user. The *GRANT* statement is used to grant users permissions to perform activities, either in general or on specific objects.

```sql
CREATE USER 'bob'@'%' IDENTIFIED BY 'test';
CREATE USER 'kate'@'%' IDENTIFIED BY 'test;'
CREATE USER 'martin'@'%' IDENTIFIED BY 'test;'
GRANT SELECT ON bob_database.* TO 'bob'@'%';
GRANT SELECT(Id), INSERT(Id, Name) ON bob_database.* TO 'kate'@'%';
GRANT ALL ON bob_database.* TO 'martin'@'%';
```

The *REVOKE* statement is the opposite of the *GRANT* statement: you can use it to revoke rights assigned using *GRANT*.

```sql
REVOKE SELECT(Id) ON bob_database.* FROM 'kate'@'%';
```

You can check what privileges / grants are assigned to user by using:

```sql
SHOW GRANTS FOR 'bob'@'%';
```