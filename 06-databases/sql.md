# Databases and SQL

61. Why can't we simply store everything in Python variables?

Variables live in a running process and usually disappear when it exits. They also are not automatically shared reliably among multiple application instances or users. Files and databases provide persistence and ways to manage shared data.

62. Why do applications need databases?

Databases store and retrieve durable, structured data, often for many users at once. They provide querying, access control, backup options, and mechanisms for handling concurrent changes that ordinary variables do not provide.

63. What happens when you click “Save”?

The application collects and validates the input, then sends it to its backend or database layer. The service checks permissions and constraints, performs a database operation, and reports success or failure; a well-designed UI only confirms a save after it receives the appropriate result.

64. Where does the data physically go?

The database writes data to files on storage devices on the database host, often using a write-ahead log and memory buffers to make writes reliable and efficient. Managed databases may replicate or distribute those files across machines and locations.

65. What is a table?

In a relational database, a table is a named collection of rows with a defined set of columns. Tables model entities or relationships, such as customers or orders.

66. What is a row?

A row is one record in a table, containing values for that record's columns. For example, a customer row might contain an identifier, name, and email address.

67. What is a column?

A column defines one attribute for rows in a table, such as `email` or `created_at`, typically with a data type and optional constraints. Each row provides a value for that attribute, or a permitted missing value.

68. Why do we need primary keys?

A primary key uniquely identifies each row so applications and other tables can refer to it reliably. A database enforces uniqueness and non-nullability for the key; it may be a generated number, UUID, or meaningful value.
