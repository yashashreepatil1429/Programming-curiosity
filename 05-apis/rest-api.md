# REST APIs

57. What are HTTP methods?

HTTP methods describe the intended action for a request. Common methods include GET to retrieve, POST to submit or create, PUT to replace, PATCH to partially update, and DELETE to remove a resource.

58. Why do we have GET, POST, PUT, PATCH, and DELETE?

They give clients and servers shared conventions about the meaning of requests and their effects. GET is intended to be safe and retrieval-oriented; PUT and DELETE are designed to be idempotent, while POST commonly performs actions that may create repeated effects.

59. What happens if an API takes 10 seconds to respond?

The client waits unless its timeout or cancellation limit is reached. Users experience delay, and server resources may remain occupied; production systems use sensible timeouts, progress feedback, retries with care, and performance monitoring.

60. What happens if the API server is completely down?

Connections fail or time out, so clients cannot get a normal response. Applications should display a clear error, avoid unsafe repeated submissions, and may use redundancy, health checks, queues, or cached data to improve resilience.
