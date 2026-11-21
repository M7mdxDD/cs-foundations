# Network Lab - Week 2

## Exercise 5: Inspect a Real Request

### Main Request
- **URL:** `https://en.wikipedia.org/wiki/Wiki`
- **Method:** `GET`
- **Status Code:** `200 OK`
- **Content-Type:** `text/html; charset=UTF-8`

**Request Headers (3):**
- `accept`: `text/html,application/xhtml+xml,application/xml;q=0.9,image/jxl,image/avif,image/webp,image/apng,*/*;q=0.8`
- `accept-language`: `ar;q=0.5`
- `user-agent`: `Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/158.0.0.0 Safari/537.36`

**Response Headers (3):**
- `accept-ranges`: `bytes`
- `age`: `88616`
- `cache-control`: `private, s-maxage=0, max-age=0, must-revalidate, no-transform`

### Different Request (Non-GET / Non-200)
- **Request:** `events?hasty=true`
- **Method:** `POST`
- **Status Code:** `202 Accepted`
- **What it is:** A background analytics/event request sending JSON payload data (such as `bot=0` and tracking IDs) to the server. The `202 Accepted` status means the server received the data and will process it later in the background without delaying the page load.

## Exercise 6: curl a Page and an API

### 1. Page Status Code & `-I` Flag
- **Status Code:** `200`
- **What `-I` shows:** It fetches and prints only the HTTP status line and response headers without the page body, whereas plain `curl` prints only the HTML body.

### 2. Pipe Command (`curl -s ... | python3 -m json.tool`)
- **Left side (`curl -s https://api.github.com/users/octocat`):** Fetches the raw JSON data from GitHub's API silently (`-s` hides the progress meter).
- **Right side (`python3 -m json.tool`):** Takes the output from `curl` via the pipe (`|`) as its input, validates the JSON, and formats it cleanly.

### 3. Non-Existent GitHub User (`curl -i`)
- **Command:** `curl -i https://api.github.com/users/mhmd99999notrealuser888`
- **Status Line:** `HTTP/2 404`
- **Shortened Output:**
  ```text
  HTTP/2 404
  content-type: application/json; charset=utf-8
  ...
  {"message": "Not Found", "status": "404"}
  ```
- **Who made the mistake?** Me — any `4xx` status code means the error is in the client request, not a server failure.

### 4. DNS & Ping Comparison (`example.com`)
- **`nslookup example.com` IPs:**
  - IPv4: `172.66.147.243`, `104.20.23.154`
  - IPv6: `2606:4700:10::ac42:93f3`, `2606:4700:10::6814:179a`
- **`ping -c 3 example.com` Output (shortened):**
  ```text
  PING example.com (172.66.147.243) 56(84) bytes of data.
  3 packets transmitted, 3 received, 0% packet loss, time 2002ms
  rtt min/avg/max/mdev = 44.754/64.979/100.043/24.891 ms
  ```
- **Comparison:** They match. `ping` resolved `example.com` to `172.66.147.243`, which is the first IPv4 address returned by `nslookup`.ٍ