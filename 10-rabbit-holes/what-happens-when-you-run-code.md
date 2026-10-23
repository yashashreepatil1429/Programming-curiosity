# Rabbit Holes 1–4

## 1. When I type `x = 10`, where exactly does `10` go?

In Python, the interpreter evaluates `10` as an integer object and binds the name `x` to it in the current namespace. The name and object are represented somewhere in the process's virtual address space; the operating system maps the process's memory to physical RAM as needed. Python does not promise a permanent address or a separate physical slot for each name. If `x` is rebound and no references to that object remain, the runtime can reclaim or reuse its memory.

**Variable → Object → Memory → RAM → Process → Operating system**

## 2. When I type `python app.py`, what happens between pressing Enter and seeing the output?

The terminal sends the command to a shell. The shell finds the `python` executable, asks the operating system to start it, and passes `app.py` as an argument. Python reads and parses the source, compiles it to bytecode, and its runtime executes that bytecode. Calls such as `print` write to a stream connected to the terminal; the process eventually exits with a status code. Syntax errors, exceptions, or OS failures can interrupt this path and produce diagnostics instead of the expected output.

## 3. When I enter `google.com`, how does my computer find another computer somewhere in the world?

The browser first checks whether it already knows a usable address. Otherwise, a DNS resolver looks up records for `google.com` and returns an IP address. The device establishes a connection to that address, typically negotiates TLS for HTTPS, and sends an HTTP request. Routers forward packets across networks toward the destination; Google's infrastructure may route the request through load balancers to a suitable server. The response travels back over the connection, and the browser interprets and renders the returned resources. DNS caching, redirects, proxies, and content-delivery systems can alter the exact route.

## 4. When I click Login, how does my password travel from my phone to the server and come back as “Login successful”?

The app sends the credentials to the service over HTTPS, which encrypts the connection in transit and authenticates the server. The server validates the input, retrieves the account's stored password hash, and checks the submitted password using the same password-hashing scheme; a secure service does not store or return the plain password. If checks succeed, it creates a session or issues a token and sends that credential to the app, typically in a protected cookie or secure storage. Later requests present the session credential, which the server verifies. Login can also require a second factor, rate limits, and other checks; “success” should reveal only the minimum information needed.
