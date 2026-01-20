# Stateless vs Stateful Services

This document explains the difference between stateless and stateful services in backend systems.
Understanding this distinction is essential for designing scalable and reliable applications.

---

## Overview

Stateless and stateful services differ in how they manage client state across requests.
This affects scalability, fault tolerance, and system complexity.

---

## Stateless Services

A stateless service does not store any client-specific information on the server.

Each request:
- Is independent
- Contains all required data
- Can be handled by any server instance

### Characteristics
- No server-side session state
- Easy horizontal scaling
- Simple load balancing
- Better fault tolerance

---

## Stateful Services

A stateful service stores client-specific state on the server between requests.

Each request:
- Depends on previously stored state
- May require session continuity
- Is tied to server-side memory or storage

### Characteristics
- Server maintains session data
- More complex scaling
- Requires session management
- Sensitive to server failures

---

## Key Differences
```
| Aspect | Stateless | Stateful |
|------|---------|---------|
Client state | Not stored on server | Stored on server |
Request handling | Independent | Dependent |
Scalability | Easy | Complex |
Load balancing | Simple | Requires sticky sessions |
Fault tolerance | High | Lower |
```
---

## Scalability Considerations

Stateless services scale easily by adding more instances.
Stateful services require shared storage or session affinity to scale effectively.

---

## Use Cases

Stateless services are commonly used in modern web APIs and microservices.
Stateful services are often found in session-driven or legacy systems.

