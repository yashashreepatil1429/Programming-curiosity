# Your First Line of Code

11. What happens internally when you write `x = 10`?

In Python, the runtime creates or obtains an integer object for `10` and binds the name `x` to that object in the current scope. Assignment is name binding, not a command to reserve a permanently named physical memory cell.

12. Where is `10` stored?

While the program runs, the integer object's data is represented in the process's virtual memory, backed by RAM as needed. The exact address and representation are implementation details and can change.

13. Where is `x` stored?

The name `x` is an entry in a namespace, such as a function's local variables or a module's globals. That namespace is part of the running process; it is not necessarily a separate memory box labeled `x`.

14. Is `x` actually the value `10`?

Conceptually, `x` refers to the integer value `10`. In Python, names refer to objects; they are not typed containers that inherently contain a value.

15. What happens when you write `x = 10` and then `x = 20`?

The name `x` is rebound to the integer object `20`. Other names that still refer to `10` remain unchanged.

16. What happens to `10`?

If no references to its object remain, it can be reclaimed. Python implementations may reuse or cache some objects, so you cannot infer exact memory reclamation just from reassignment.

17. What happens when you write `a = b = c = 100`?

Python evaluates the right-hand expression and binds all three names to its result. This is one assignment statement, not a request to make independent copies.

18. Are `a`, `b`, and `c` three copies of `100`?

They refer to the same integer object at that moment. Integers are immutable, so sharing is safe: an operation that appears to change one name creates or selects another value and rebinds that name rather than modifying the shared integer.

19. What happens to variables when a function finishes?

The function's local namespace stops being active when it returns. Objects reachable only through those locals can be reclaimed, but objects returned or saved elsewhere remain available.

20. Who cleans up unused memory?

The language runtime and operating system manage different layers. In CPython, reference counting and a cyclic garbage collector reclaim many unreachable objects; the OS manages the process's memory pages and may retain released memory for reuse.
