# HTTP and HTTPS

## Overview
This document explains the core concepts of **HTTP and HTTPS** from a backend interview perspective.  
The focus is on **statelessness, request–response flow, security, and TLS handshake**, based strictly on handwritten notes.

---

## HTTP

### Definition
HTTP (HyperText Transfer Protocol) is a **stateless, application-layer protocol** used for communication between a **client and a server** using a **request–response model**.

### Important Points
- Runs on top of **TCP**
- Text-based protocol
- Stateless by default
- Client initiates every request

---

## Statelessness

### What does stateless mean?
- Server does **not store client session state**
- Each request is **independent**
- All required information must be present in the request

### Then how do sessions work?
Although HTTP is stateless, sessions are managed using:
- Cookies
- Session IDs
- JWT Tokens

---

## HTTP Request Flow

1. Client opens TCP connection
2. Client sends HTTP request:
   - Method (GET, POST, etc.)
   - URI
   - Headers
   - Optional body
3. Server processes the request
4. Server sends HTTP response:
   - Status code
   - Headers
   - Body
5. Connection is closed or kept alive

---

## HTTP Methods

| Method | Purpose | Idempotent |
|------|--------|-----------|
| GET | Fetch data | Yes |
| POST | Create resource | No |
| PUT | Replace resource | Yes |
| PATCH | Partial update | No |
| DELETE | Remove resource | Yes |

---

## HTTP Status Codes

| Range | Meaning |
|-----|--------|
| 2xx | Success |
| 3xx | Redirection |
| 4xx | Client Error |
| 5xx | Server Error |

---

## HTTPS

### What is HTTPS?
HTTPS is **HTTP with TLS encryption**.

### What does HTTPS ensure?
- **Confidentiality** (data is encrypted)
- **Integrity** (data is not modified)
- **Authentication** (server identity is verified)

---

## TLS Handshake (High Level)

1. Client sends supported encryption methods
2. Server sends certificate
3. Client verifies certificate
4. Secure key exchange happens
5. Encrypted communication starts

---

## HTTP vs HTTPS

| Feature | HTTP | HTTPS |
|------|----|------|
| Encryption | No | Yes |
| Port | 80 | 443 |
| Security | Unsafe | Secure |
| Performance | Slightly faster | Slight overhead |

---

## Interview Notes
- HTTP is stateless, but state is managed at application level
- HTTPS is mandatory for secure communication
- TLS uses asymmetric encryption for key exchange and symmetric encryption for data transfer

---

## Handwritten Notes Reference

![notes](notes.jpg)

