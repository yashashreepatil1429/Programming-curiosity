# DNS

41. What happens when you type `google.com` into a browser?

The browser checks its caches and asks DNS for an address if needed, then establishes a network connection to a server and sends an HTTP or HTTPS request. The server responds with page data and resources, which the browser parses and renders. Redirects, caches, proxies, and many servers may be involved.

42. How does your computer find Google's server?

DNS returns one or more IP addresses for the domain, often using nearby resolvers and cached answers. The network routes packets toward an address; load balancers and Google's infrastructure can choose which actual server handles the connection.

43. What is DNS?

The Domain Name System is a distributed naming system that maps domain names such as `google.com` to records including IP addresses. It lets people use names instead of memorizing addresses, and its answers can change or be cached for a limited time.
