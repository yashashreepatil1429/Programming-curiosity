# Authentication

71. How does a website know who you are after login?

The site verifies a login factor, such as a password or passkey, and then creates a session. The browser sends a session cookie or token with later requests so the server can associate them with that authenticated session; it should expire and be protected against theft.

72. Where is your password stored?

For a properly designed service, the password is not stored as readable text. The service stores a salted password hash produced by a slow password-hashing algorithm, ideally with its algorithm and work parameters, in a protected credential store.

73. Why shouldn't passwords be stored as plain text?

A database leak would immediately reveal every password, including passwords reused on other sites. A unique salt and password-specific hash such as Argon2id, scrypt, or bcrypt makes stolen records much harder to use; ordinary fast hashes like SHA-256 are not suitable for password storage by themselves.

79. What is a token?

A token is a value a client presents to prove or carry some authorization context. A session identifier may be an opaque random value checked by the server, while a signed token may carry claims; signatures do not encrypt claims, so tokens must be scoped, validated, stored, and expired appropriately.
