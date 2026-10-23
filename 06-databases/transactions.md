# Database Transactions

A transaction groups database operations into one logical unit. The database attempts to make the unit atomic (all or none), consistent with its constraints, isolated from conflicting work, and durable after commit—the familiar ACID properties.

When two users update the same record concurrently, the database may serialize their work with locks, detect a conflict, or use a concurrency-control strategy such as multiversion concurrency control. Depending on the isolation level, one update may wait or fail and need to be retried; the application must avoid silently overwriting important changes.

See also [rabbit hole 7](../10-rabbit-holes/what-happens-when-you-open-google.md).
