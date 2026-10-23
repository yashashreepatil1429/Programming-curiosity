# What Is an API?

51. What exactly is an API?

An Application Programming Interface is a defined way for software to request services or data from other software. It may be a library's functions, an operating-system interface, or a network service such as a web API.

52. Why can't two applications simply access each other's variables?

Separate applications usually run in isolated process memory, so one cannot safely or reliably read another's variables. An API provides an agreed, validated interface for exchanging data while preserving each application's control and boundaries.

53. What happens when a React application calls a Node or Python API?

The browser's JavaScript sends a network request, usually over HTTP, to a server endpoint. The server validates the request, runs application logic, may access other services or a database, and returns a response—often JSON—which the React application uses to update the interface.
