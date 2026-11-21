# Exercise 7: The URL Story

## What Happens When You Type a URL and Press Enter (10 Steps)

1. The browser splits the URL into its parts (protocol, domain, path).
2. The browser checks its caches to see if the answer is already saved.
3. DNS translates the domain name into an IP address.
4. The browser opens a TCP connection to the server on port 443 (HTTPS).
5. TLS sets up encryption so the connection is secure.
6. The browser sends an HTTP request (`GET /path`) along with headers.
7. The server (often behind a load balancer) receives the request.
8. The app on the server runs its code and may query a database.
9. The server sends back an HTTP response with a status code, headers, and the HTML.
10. The browser parses the HTML, sends new requests for CSS, JS, and images (repeating steps 3–9), and draws the page on the screen.

## What I Missed on My First Attempt
- Completely forgot **step 6** (sending the actual HTTP `GET` request with headers) and **step 8** (the server running app code / querying a database).
- Forgot to explicitly mention **DNS** (step 3), **TCP** (step 4), and **TLS / encryption** (step 5).
- Missed the details of what the server returns (status, headers, HTML) and that the browser makes extra requests for CSS, JS, and images before drawing the page.