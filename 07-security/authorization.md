# Authorization

76. What happens if someone changes an API request?

The server receives whatever the client sends, so it must validate all inputs and independently enforce permissions. TLS helps prevent in-transit tampering, but it cannot make a client trustworthy; altered data should be rejected or safely handled, and sensitive actions should be logged.

77. What is CORS?

Cross-Origin Resource Sharing is a browser-enforced policy that uses HTTP headers to decide whether a web page from one origin may read a response from another. It is not authentication or a server-side firewall: non-browser clients can send requests, so APIs still need authentication, authorization, and input validation.

78. How does a server know whether you are authorized?

The server authenticates the caller, identifies the requested resource and action, then checks permissions or policy for that user, role, or service. It should make this check on every protected operation rather than trusting hidden buttons or client-side state.

80. How can one careless line of code expose millions of users?

A small mistake—such as skipping an access check, logging secrets, or building a query unsafely—can be repeated across many requests or records. Secure defaults, code review, testing, least privilege, monitoring, and incident response reduce the chance and impact, but no single safeguard is enough.
