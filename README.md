# API Fundamentals — Quick README

**Source:** Postman API Fundamentals Student Expert certification. :contentReference[oaicite:0]{index=0}

## What this is
A concise reference for basic API concepts and common Postman workflows: making requests (GET/POST/PATCH/DELETE), using variables, adding auth, reading responses, and simple scripting with Postman’s `pm` API.

## Prerequisites
- Postman installed (or an HTTP client / curl)
- Basic familiarity with JSON and HTTP

## Core concepts (one-line)
- **API:** a contract for code-to-code communication. :contentReference[oaicite:1]{index=1}  
- **Request:** method + URL (+ headers, params, body). :contentReference[oaicite:2]{index=2}  
- **Response:** status code (2xx, 4xx, 5xx) + body. :contentReference[oaicite:3]{index=3}

## Quick start examples
**GET**

curl -X GET "https://library-api.postmanlabs.com/books"
POST (JSON body)

curl -X POST "https://library-api.postmanlabs.com/books" \
  -H "Content-Type: application/json" \
  -d '{"title":"My Book","author":"Me"}'
PATCH (path variable)

curl -X PATCH "https://library-api.postmanlabs.com/books/:id" \
  -H "Content-Type: application/json" \
  -d '{"checkedOut": true}'
DELETE

curl -X DELETE "https://library-api.postmanlabs.com/books/:id"
(Expect 204 No Content on success.) 
Postman API Fundamentals Studen…


## Authorization & Headers
**Common auth**: API Key, Basic Auth, OAuth. Put API keys in headers (e.g., api-key: postmanrulz) or use Postman Authorization helper. 
Postman API Fundamentals Studen…

## Variables (Postman)
Use {{baseUrl}}, {{id}} to avoid repetition.

**Scopes**: global → collection → environment → data → local. Current value resolves at runtime. 
Postman API Fundamentals Studen…

## Simple Postman scripting
**Access response JSON**: const body = pm.response.json();

**Set collection variable**: pm.collectionVariables.set("id", body.id);

Use in later requests as {{id}}. 
Postman API Fundamentals Studen…

## Tips
**Read API docs for required path vs query params.**
Postman API Fundamentals Studen…

**Use Postman Console for debugging requests and scripts.**
Postman API Fundamentals Studen…

## Further reading
**Postman docs and the Library API examples referenced in the course.**
Postman API Fundamentals Studen…
