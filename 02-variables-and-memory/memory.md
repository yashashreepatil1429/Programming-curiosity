# Memory — The Hidden World

21. What is RAM actually doing while your program runs?

RAM temporarily holds the instructions and data the processor needs to access quickly. The operating system gives each process a virtual address space and maps portions of it to physical memory or, under pressure, other backing storage.

22. What is the difference between RAM and storage?

RAM is fast working memory that is generally cleared when power is lost; storage such as an SSD keeps files when the computer is off but is slower. Programs are loaded from storage into memory to run.

23. Where does a Python variable live?

A Python name lives in a namespace managed by the interpreter. Its referenced object and the namespace data occupy the process's memory, but Python abstracts away their exact physical locations.

24. What is a memory address?

An address identifies a location in a process's address space. Modern operating systems usually provide virtual addresses, which are translated to physical memory; addresses can differ between runs and processes.

25. Why can't we normally see memory addresses in Python?

Python hides low-level representation to make programs safer and more portable. You can inspect an object's identity with `id()`, but Python does not promise that it is a physical address or that it stays fixed.
