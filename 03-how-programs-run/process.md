# Processes

33. What is a process?

A process is a running program with its own operating-system-managed resources, including a virtual address space, open files, and security identity. The OS schedules its threads to use the processor.

40. What happens when the program crashes?

An unhandled error may make the runtime print a traceback and exit with a nonzero status. A severe fault may cause the OS to terminate the process; its resources are cleaned up, but unsaved work may be lost. Logs and error handling help diagnose and recover.
