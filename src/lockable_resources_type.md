# Lock, Lockable resources type

## Lock

* By default, most of the database managment softwares uses a pure locking model to enforce the isolation property of transactions.
* Locks are control resources obtained by a transaction to guard data resources, preventing conflicting or incompatible access by other transactions.
* Exclusive locks are called "exclusive" because you cannot obtain an exclusive lock on a resource if another transaction is holding any lock mode on the resource (not possible to read and update). An exclusive lock permits the transaction that holds the lock to update or delete a row.
* Shared locks - When you try to read data, by default your transaction requests a shared lock on the data resource and releases the lock as soon as the read statement is done with that resource. This lock mode is called "shared" because multiple transactions can hold shared locks on the same data resource simultaneously. A shared lock permits the transaction that holds the lock to read a row.

## Lockable resources types

* Server can lock different types of resources. Those include rows (RID in a heap, key in an index) pages, objects (for example, tables), databases, and others.
* In most cases lock are managed by Server and locks can be differ depend on number or records.
* When one transaction holds a lock on a data resource and another transaction requests an incompatible lock on the same resource, the request is blocked and the requester enters a wait state.