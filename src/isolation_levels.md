# Isolation levels

* The isolation level is the setting that balances performance, reliability, consistency, and reproducibility of results when multiple transactions are making changes and performing queries simultaneously.
* The SQL:1992 standard defines four classic isolation levels, and MySQL supports all of them:
  * REPEATABLE READ - all queries within the transaction will see the same snapshot of the data, established by the first read (it is default)
  * READ COMMITTED - each consistent read, even within the same transaction, creates and reads its own fresh snapshot.
  * READ UNCOMMITTED - in this isolation level MySQL performs SELECT statements in a non-locking fashion, which means two SELECT statements within the same transaction might not read the same version of a row.
  * SERIALIZABLE - the most restricted isolation level available in MySQL is SERIALIZABLE. This is similar to REPEATABLE READ, but has an additional restriction of not allowing one transaction to interfere with another. 
* A user can also change the isolation level for a single session or all subsequent connections with the statement *SET [GLOBAL/SESSION] TRANSACTION*.

Let's look at examples :)