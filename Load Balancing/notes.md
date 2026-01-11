# Load Balancing

This document explains the **core concept of load balancing** in backend systems.
Load balancing is used to distribute incoming requests across multiple servers to improve performance, scalability, and reliability.

---

## Overview

Load balancing is the process of **evenly distributing client requests** among multiple backend servers so that no single server becomes a bottleneck.

It is a fundamental concept in building scalable and highly available backend systems.

---

## Why Load Balancing Is Needed

Without load balancing:
- All requests are handled by a single server
- The server can become overloaded
- A single server failure can bring down the system

With load balancing:
- Traffic is distributed across multiple servers
- The system can handle higher load
- Failure of one server does not stop the application

---

## Basic Load Balancing Flow

1. Client sends a request
2. Request reaches a load balancing layer
3. One backend server is selected
4. The request is forwarded to that server
5. Server processes the request
6. Response is returned to the client

The client is unaware of how many backend servers exist.

---

## Types of Load Balancing

### 1. Client-Side Load Balancing

- The client decides which server to send the request to
- The client is aware of multiple server instances
- Requires service discovery on the client side

This approach increases complexity on the client.

---

### 2. Server-Side Load Balancing

- Client sends requests to a single entry point
- Load balancing logic runs on the server side
- Backend server details are hidden from the client

This is the most commonly used approach.

---

## Load Balancing Algorithms

Load balancing algorithms determine how requests are distributed.

### Common Algorithms

- **Round Robin**  
  Requests are distributed sequentially across servers.

- **Least Connections**  
  Requests are sent to the server with the fewest active connections.

- **IP Hash**  
  Requests from the same client IP are routed to the same server.

Each algorithm is chosen based on traffic patterns and system requirements.

---

## Stateless and Stateful Services

Load balancing works best with **stateless services**.

- Stateless services do not store client-specific data
- Any server can handle any request

Stateful services may require:
- Sticky sessions
- Shared session storage
- External state management

Designing stateless services simplifies load balancing.

---

## Benefits of Load Balancing

- Improves application availability
- Enables horizontal scaling
- Prevents server overload
- Increases fault tolerance
- Provides a single access point for clients

---

## Key Characteristics

- Transparent to clients
- Works with multiple backend servers
- Supports scalability and reliability
- Essential for modern backend architectures

---
