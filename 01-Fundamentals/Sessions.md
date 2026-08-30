# Sessions

## Definition

A session is a server-side mechanism used to maintain a user's state across multiple HTTP requests.

HTTP is stateless, so applications need session management to recognize authenticated users across different requests.

---

## Why Sessions Are Needed

Without session management, a server would not automatically know that multiple requests belong to the same authenticated user.

Sessions allow applications to maintain information such as:

- User identity
- Authentication state
- User role
- Session lifetime

---

## Cookie vs Session

| Cookie | Session |
|---|---|
| Usually stored in the browser | Usually maintained on the server |
| Sent by the browser with requests | Contains server-side user state |
| Can store small pieces of data | Maintains application state |
| Example: session identifier | Example: authenticated user state |

A common implementation stores the **Session ID in a Cookie** while the actual session data is maintained server-side.

---

## Login and Session Flow

```text
Client
   │
   │ POST /login
   ▼
Server
   │
   │ Verify Credentials
   ▼
Authentication
   │
   │ Valid
   ▼
Create Session
   │
   │ Session ID
   ▼
Set-Cookie
   │
   ▼
Client
   │
   │ GET /profile
   │ Cookie: session=ABC123
   ▼
Server
   │
   │ Find Session
   ▼
Authenticated User
```

---

## Session ID

A Session ID is an identifier used by the server to associate a client with server-side session data.

Example:

```text
session=ABC123
```

The browser generally stores the identifier rather than the complete authentication state.

---

## Session Storage

Session data may be stored using different mechanisms depending on the application's architecture, including:

- Server-side files
- Databases
- In-memory stores
- Redis

---

## Session Hijacking

Session Hijacking occurs when an attacker obtains a valid user's Session ID and attempts to use it to impersonate that user.

Potential impacts include:

- Unauthorized account access
- Account impersonation
- Access to protected resources

---

## Session Fixation

Session Fixation occurs when an attacker attempts to make a victim use a session identifier that the attacker already knows or controls.

A key mitigation is regenerating the session identifier after successful authentication.

---

## Session Security

Important security practices include:

- Use HTTPS
- Use the Secure cookie attribute
- Use the HttpOnly cookie attribute
- Use the SameSite cookie attribute
- Regenerate session identifiers after authentication
- Implement appropriate session timeouts
- Invalidate sessions during logout

---

## Why Sessions Matter in Cyber Security

Session management is closely related to:

- Authentication
- Authorization
- Session Hijacking
- Session Fixation
- Cross-Site Scripting (XSS)
- Cross-Site Request Forgery (CSRF)

---

## Key Takeaways

- HTTP is stateless.
- Sessions allow applications to maintain user state across requests.
- Session data is generally maintained server-side.
- A Session ID is commonly stored in a browser Cookie.
- Session IDs should be treated as sensitive authentication material.
- Secure session management is essential for Web Application Security.

---

## References

- OWASP Authentication Cheat Sheet
- OWASP Session Management Cheat Sheet
- MDN Web Security Documentation
- PortSwigger Web Security Academy