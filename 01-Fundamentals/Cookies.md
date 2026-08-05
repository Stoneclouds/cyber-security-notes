# Cookies

## Definition

A cookie is a small piece of data stored by the browser at the request of the server. Cookies help websites remember users across multiple HTTP requests.

---

## Why Cookies Are Needed

HTTP is a stateless protocol. Without cookies, the server would treat every request as coming from a new user.

Cookies allow websites to remember:

- Logged-in users
- Language preferences
- Theme settings
- Shopping carts

---

## Cookie Flow

```text
Client
   │
POST /login
   │
Server
   │
Set-Cookie: session=ABC123
   │
Browser stores Cookie
   │
GET /profile
Cookie: session=ABC123
   │
Server recognizes the user
```

---

## Types of Cookies

### Session Cookie

- Stored temporarily
- Deleted when the browser closes

### Persistent Cookie

- Stored until expiration
- Used for "Remember Me" functionality

---

## Cookie Security Attributes

### Secure

Only sends cookies over HTTPS.

### HttpOnly

Prevents JavaScript from accessing cookies.

### SameSite

Helps mitigate Cross-Site Request Forgery (CSRF).

---

## Why Cookies Matter in Cyber Security

Cookies are essential for user authentication and session management.

Improperly protected cookies can lead to:

- Session Hijacking
- Cross-Site Scripting (XSS)
- Cross-Site Request Forgery (CSRF)

---

## Key Takeaways

- Cookies are stored in the browser.
- Cookies usually store a session identifier, not the user's password.
- Secure, HttpOnly, and SameSite improve cookie security.
- Cookies enable websites to recognize authenticated users.

---

## References

- MDN Web Docs
- OWASP Cheat Sheet Series
- OWASP Top 10