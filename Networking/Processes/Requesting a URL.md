URL = universal Resource Locator
Scheme: `http://`, `https://`
Domain: `example.com`
Path: `product/electric`
Resource: `phone`

Difference between Path and Resource is like file directories and files.

1. When a URL is entered, the domain is looked up in a DNS server. 
	The browser may look for this is the DNS Cache to speed up fetching this information
	If the domain is not found in the DNS Cache, it recursively looks for the domain in other servers using the DNS Resolver.
2. Once the domain's IP Address has been found, a TCP connection is established with the server. If the browser is using HTTPS, protocols like TLS handshake is used to resolve this.
3. Browser now sends requests to the server through HTTP
4. The server sends back responses through HTTP
5. The Browser now renders the HTTP data received.