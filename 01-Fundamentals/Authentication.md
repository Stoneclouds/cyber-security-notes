# Authentication

## Definition

Authentication is the process of verifying the identity of a user or other entity.

It answers the question:

> Who are you?

---

## Authentication vs Authorization

### Authentication

Determines the identity of a user.

> Who are you?

### Authorization

Determines what an authenticated user is allowed to access or perform.

> What are you allowed to do?

---

## Common Credentials

Examples include:

- Username and Password
- Passkeys
- One-Time Passwords (OTP)
- Security Tokens
- Digital Certificates
- Biometrics

---

## Login Flow

```text
User
   │
   │ Credentials
   ▼
Client
   │
   │ POST /login
   ▼
Server
   │
   │ Verify Credentials
   ▼
Database
   │
   │ Valid
   ▼
Server
   │
   │ Create Session
   ▼
Session ID
   │
   ▼
Client Cookie
```

---

## Password Storage

Passwords should not be stored as plaintext.

Instead, applications should use secure password hashing.

```text
Password
   ↓
Password Hashing
   ↓
Stored Hash
```

Examples of modern password-hashing algorithms include:

- Argon2
- bcrypt

---

## Multi-Factor Authentication (MFA)

MFA requires multiple authentication factors.

### Something You Know

- Password
- PIN

### Something You Have

- Phone
- Hardware Security Key

### Something You Are

- Fingerprint
- Facial Recognition

---

## Authentication and Sessions

Authentication verifies the user's identity.

After successful authentication, an application may create a session to maintain the user's authenticated state across subsequent HTTP requests.

```text
Credentials
   ↓
Authentication
   ↓
Success
   ↓
Session Created
   ↓
Session ID
```

---

## Common Authentication Risks

- Weak passwords
- Brute-force attacks
- Credential stuffing
- Insecure session management
- Weak password-reset mechanisms
- Missing or weak MFA

---

## OWASP Top 10

Authentication security is closely related to:

**A07:2021 - Identification and Authentication Failures**

SQL Injection is related to:

**A03:2021 - Injection**

---

## Security Best Practices

- Use strong password hashing.
- Enforce HTTPS.
- Implement secure session management.
- Regenerate session identifiers after authentication.
- Apply rate limiting.
- Implement MFA where appropriate.
- Monitor suspicious authentication activity.

---

## Key Takeaways

- Authentication verifies identity.
- Authorization determines permissions.
- Passwords should be securely hashed.
- Successful authentication commonly leads to session creation.
- Authentication weaknesses can lead to account compromise.

---

## Related Topics

- Cookies
- Sessions
- Authorization
- SQL Injection
- Broken Access Control
- Multi-Factor Authentication

---

## References

- OWASP Authentication Cheat Sheet
- OWASP Top 10
- MDN Web Security Documentation
- PortSwigger Web Security Academy