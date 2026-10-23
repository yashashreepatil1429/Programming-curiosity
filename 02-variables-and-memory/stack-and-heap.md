# Stack and Heap

26. What is a stack?

A stack is a last-in, first-out structure used by runtimes to manage active function calls and their local execution state. When a function calls another function, a new call frame is added; returning removes that frame. Exact storage details vary by language and implementation.

27. What is a heap?

The heap is a common name for memory used for objects whose lifetime is not tied to one simple call frame. In Python, objects are generally managed by the runtime, and it is misleading to assume every object has a directly inspectable, fixed “heap address.”
