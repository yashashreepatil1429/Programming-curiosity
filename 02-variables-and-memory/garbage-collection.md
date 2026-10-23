# Garbage Collection

28. What is garbage collection?

Garbage collection is automatic detection and reclamation of memory occupied by objects the program can no longer reach. It reduces the need for programmers to free each object manually, though it does not prevent every memory leak.

29. Why doesn't unused memory remain forever?

The runtime reuses memory so long-running programs do not endlessly consume more space for objects they no longer need. Reclaimed memory may remain reserved by the runtime for future allocations instead of immediately being returned to the operating system.

30. What happens when your program consumes too much memory?

The OS may slow down as it moves memory pages to storage, allocation may fail, or the process may be terminated. The exact outcome depends on the OS, available memory, and runtime; programs should release references and process large data carefully.
