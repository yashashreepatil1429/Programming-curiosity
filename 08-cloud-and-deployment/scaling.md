# Scaling

93. What changes when one million users use your application?

Traffic, concurrent connections, storage, and failure rates increase, often unevenly. Teams must measure bottlenecks, protect shared services, distribute load, cache where safe, and plan capacity; multiplying servers alone does not fix a database or design bottleneck.

94. Why can't we simply buy one huge computer?

A larger machine has practical limits, can be expensive, and remains a single point of failure. Multiple machines can scale capacity and improve availability, but introduce network latency, coordination, consistency, and operational complexity.

99. How does Netflix, YouTube, or Instagram handle millions of users?

Large services use many layers: geographically distributed data centres, load balancing, caching and content delivery networks, partitioned services and databases, queues, and monitoring. Exact designs differ and evolve; their scale comes from distributed systems, redundancy, and continual capacity and reliability work.

100. If you had to build WhatsApp from scratch, what would you need?

You would need clients, identity and contact management, secure message protocols, real-time connections, message routing and delivery queues, durable storage, push notifications, media storage, abuse prevention, and monitoring. You would also need end-to-end encryption with carefully designed key management, privacy and safety processes, and a way to handle offline users and device changes. Start with a small reliable service, then scale based on measured needs.
