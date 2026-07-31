# HTTPS (Hypertext Transfer Protocol Secure)

## Definition

HTTPS (Hypertext Transfer Protocol Secure) is the secure version of HTTP. It protects communication between clients and servers by using TLS (Transport Layer Security) to encrypt transmitted data.

---

## Why HTTPS Exists

HTTP sends data in plain text. This means anyone who can intercept the network traffic may be able to read sensitive information such as usernames, passwords, or session cookies.

HTTPS was introduced to solve this problem by encrypting communication.

---

## HTTP vs HTTPS

| HTTP | HTTPS |
|------|--------|
| No encryption | Encrypted using TLS |
| Port 80 | Port 443 |
| Less secure | More secure |
| Suitable for public information | Suitable for sensitive information |

---

## How HTTPS Works

```text
Browser
     │
TLS Handshake
     │
     ▼
Server
     │
Encrypted Communication
     │
     ▼
Browser
```

Before exchanging data, the client and server perform a TLS Handshake to establish a secure connection.

---

## TLS (Transport Layer Security)

TLS is a security protocol that provides:

- Encryption
- Authentication
- Data Integrity

TLS replaces the older SSL protocol, which is now considered outdated.

---

## Encryption

Without HTTPS

```text
Username : cliffton
Password : 123456
```

Anyone intercepting the communication could potentially read this information.

With HTTPS

```text
a82JKs91Lka!92...
```

The data is encrypted before being transmitted over the network.

---

## Digital Certificate

A Digital Certificate is used to verify the identity of a website.

It contains information such as:

- Domain Name
- Public Key
- Issuer
- Validity Period

The browser verifies the certificate before establishing a secure connection.

---

## Certificate Authority (CA)

A Certificate Authority (CA) is a trusted organization that issues digital certificates.

Examples:

- DigiCert
- GlobalSign
- Sectigo
- Let's Encrypt

Browsers trust these organizations to verify website identities.

---

## Man-in-the-Middle (MITM) Attack

A Man-in-the-Middle attack occurs when an attacker attempts to intercept communication between a client and a server.

HTTPS helps protect against this attack by encrypting data and verifying the server's identity.

---

## Why HTTPS Matters in Cyber Security

HTTPS is essential because many security mechanisms depend on secure communication.

Examples include:

- Secure Login
- Online Banking
- Session Cookies
- JWT Authentication
- API Communication

Without HTTPS, sensitive information could be exposed during transmission.

---

## Key Takeaways

- HTTPS is HTTP secured with TLS.
- TLS encrypts communication between clients and servers.
- HTTPS verifies server identity using Digital Certificates.
- Certificate Authorities (CAs) issue trusted certificates.
- HTTPS protects against eavesdropping and helps reduce the risk of Man-in-the-Middle attacks.

---

## References

- https://developer.mozilla.org/en-US/docs/Web/HTTP
- https://developer.mozilla.org/en-US/docs/Web/Security
- https://owasp.org/www-project-top-ten/
- https://letsencrypt.org/