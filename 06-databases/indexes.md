# Database Indexes

69. Why do we need indexes?

An index is an auxiliary structure that helps a database find rows without scanning the whole table, much like a book's index. It can speed up reads and enforce some constraints, but it consumes storage and makes inserts, updates, and deletes more expensive because the index must also be maintained.
