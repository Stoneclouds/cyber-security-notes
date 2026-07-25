# HTTP (Hypertext Transfer Protocol)

## Definition

HTTP is the communication protocol used by clients and servers to exchange information on the web.

---

## Communication Flow

```text
Client
   │
HTTP Request
   │
Server
   │
HTTP Response
   │
Client
```

---

## HTTP Methods

| Method | Purpose |
|--------|---------|
| GET | Retrieve data |
| POST | Submit data |
| PUT | Update existing data |
| DELETE | Remove data |

---

## Common Status Codes

| Code | Meaning |
|------|---------|
| 200 | OK |
| 301 | Moved Permanently |
| 302 | Temporary Redirect |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal Server Error |

---

## HTTP Headers

Headers contain additional information about the request or response, such as:

- User-Agent
- Host
- Cookie
- Content-Type
- Authorization

---

## Why HTTP Matters in Cyber Security

Most web vulnerabilities involve HTTP communication, including:

- SQL Injection
- Cross-Site Scripting (XSS)
- Cross-Site Request Forgery (CSRF)
- Authentication Bypass
- Session Hijacking

---

## Summary

HTTP is the foundation of web communication. Understanding HTTP requests, responses, methods, headers, and status codes is essential for Web Application Security.

---

## References

- MDN Web Docs
- OWASP
- PortSwigger Web Security Academy