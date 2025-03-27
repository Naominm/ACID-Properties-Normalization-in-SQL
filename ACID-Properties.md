# ACID Properties & Normalization in SQL
## ACID properties
ACID properties is the most important part od database. ACID stands for Atomicity Consistency Isolation Durability.

### Atomicity
This means that "all or nothing". When an update occurs to a database either all or none of the update will become available to anyone beyond the user. 

This update to the database is called a transaction and it either commits or aborts.

### Consistency
It ensures that any changes to values in  an instance are consistent with changes to other values in the same instance.

### Isolation
 Isolation is needed when there are concurrent transactions. Concurrent transactions are transactions that occur at the same time, such as shared multiple users accessing shared objects.

 Transactions are serializable when the effect on the database is the  same whether the transactions are executed in serial order or an interleaved fashion. 

 ### Durability
 Maintaining updates of committed transactions is important. These updates are never lost. The ACID property of durability addressed this need. Durability refers to the ability of the system to recover  committed transactions updates if either the system or he storage media fails.