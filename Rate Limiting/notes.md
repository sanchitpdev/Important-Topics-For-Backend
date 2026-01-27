# Rate Limiting

This document explains the concept of rate limiting in backend systems.
Rate limiting is used to control how many requests a client can send within a given time period.

---

## Overview

Rate limiting restricts the number of requests allowed from a client over a specific duration.
It protects backend services from overload and ensures fair resource usage.

---

## Why Rate Limiting Is Important

Rate limiting helps to:
- Prevent server overload
- Protect against abuse and attacks
- Ensure fair access for all clients
- Improve reliability and availability
- Control backend resource consumption

---

## How Rate Limiting Works

A rate limiter enforces rules such as:
- Requests per second
- Requests per minute
- Quotas per user or IP address

If a client exceeds the limit, the server may reject requests temporarily.
A common response is:
429 Too Many Requests

---

## Common Approaches

### Fixed Window Limiting

Requests are counted within a fixed time window.
Example: 100 requests per minute.

---

### Sliding Window Limiting

Requests are measured over a rolling time window.
This provides smoother enforcement than fixed windows.

---

### Token Bucket Algorithm

Tokens are added to a bucket at a constant rate.
Each request consumes a token, allowing controlled bursts.

---

### Leaky Bucket Algorithm

Requests are processed at a steady rate.
Excess requests may be queued or dropped.

---

## Where Rate Limiting Is Applied

Rate limiting can be implemented at:
- API gateway level
- Reverse proxy level
- Application level
- Per-user or per-IP level

---

## Benefits

- Protects backend systems from traffic spikes
- Prevents misuse and brute-force attempts
- Improves stability and fairness
- Reduces unnecessary load

---

## Challenges

- Setting appropriate limits
- Supporting distributed systems
- Managing shared counters across servers
- Avoiding blocking legitimate clients

