# Cloud Computing

96. What is cloud computing?

Cloud computing provides computing resources—such as servers, storage, databases, and networking—on demand through provider-managed infrastructure. It can reduce the need to buy and operate physical hardware, but customers still manage their application, configuration, data, and costs.

97. What is AWS or Azure actually providing?

Providers such as AWS and Azure offer data-centre hardware, virtual machines, storage, networks, databases, identity tools, and higher-level managed services through APIs and consoles. The provider manages some layers; responsibility for security and operations is shared and depends on the service.

98. What happens when a server crashes?

Requests sent to that instance may fail until a health check or monitoring system detects the problem. A load balancer can route traffic to healthy instances, and orchestration may restart or replace the failed one; recovery depends on redundancy, data replication, and tested procedures.
