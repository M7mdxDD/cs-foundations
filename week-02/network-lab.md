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