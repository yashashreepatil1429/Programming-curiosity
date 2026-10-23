# Rabbit Holes 8–10

## 8. How does a program know that another program has crashed?

The operating system can report that a local process exited and provide an exit status, or a parent process can wait for that event. For a remote service, there is no guaranteed instant signal: a monitor infers failure from missed health checks, timeouts, or a closed connection. A slow network can look like a crash, so systems use timeouts, retries, and health thresholds rather than assuming every missed response proves the process is dead.

## 9. If Python, JavaScript, and Java are completely different languages, how can they communicate with each other?

They agree on a boundary rather than sharing language variables directly. For example, a JavaScript client can send JSON over HTTP to a Python service, which can call a Java service through another API. They can also use message queues, files, subprocess pipes, or a native interface such as a C ABI. Each side must agree on the protocol, data format, errors, and versioning; a language-neutral boundary lets each service use a different implementation.

## 10. If the Internet disappeared tomorrow, which parts of your application would still work?

Anything that runs locally and does not depend on remote services may continue to work: the user interface, cached content, local calculations, and data saved on the device. Features needing remote login, APIs, synchronization, cloud databases, or online media would fail or become stale. Apps designed for offline use can queue changes locally and synchronize later, but must handle conflicts and protect local data. The result depends on which dependencies are on-device, on a local network, or reachable only through the public Internet.
