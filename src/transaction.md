# Transaction

* In a database, a transaction is simply a mechanism to ensure and verify that data gets to its intended destination. Just like a purchase or bank transaction, both parties must be satisfied with the results based upon some kind of pre-defined rule.
* A transaction defines the scope or context of one or more database actions.
* A transaction is a unit of work that might include multiple activities that query and modify data and that can also change the data definition.

In short (or maybe in long):

*A transaction is an operation performed (using one or more SQL statements) on a database as a single logical unit of work. All the SQL statements’ modifications in a transaction are either committed (applied to the database) or rolled back (undone from the database) as a unit, never only partially. A database transaction must be atomic, consistent, isolated, and durable*