# Request–Response Lifecycle

This document explains the **request–response lifecycle**, which describes how a client and server communicate in web-based systems.
Understanding this lifecycle is essential for backend development and API design.

---

## Overview

The request–response lifecycle represents the complete flow of:
- A request sent by a client
- Processing of that request by a server
- A response returned back to the client

Each request follows this lifecycle independently.

---

## High-Level Flow

1. Client sends a request
2. Server receives and processes the request
3. Server sends a response
4. Client receives and handles the response

This cycle is repeated for every interaction between client and server.

---

## Detailed Lifecycle Steps

### 1. Client Initiates the Request

A client (such as a browser, mobile application, or API client) creates a request that includes:
- Target URL
- Request method
- Headers
- Optional request body

The client always initiates communication.

---

### 2. Network and Connection Handling

- Domain name is resolved to an IP address
- A connection is established between client and server
- The request is transmitted over the network

These steps are handled by the underlying networking layers.

---

### 3. Server Receives the Request

- The server accepts the incoming request
- The request is passed to the web or application server
- Routing logic determines which handler should process the request

No business logic is executed at this stage.

---

### 4. Request Processing

During request processing, the server may:
- Authenticate and authorize the client
- Validate request data
- Execute business logic
- Interact with databases or external services

This step determines the outcome of the request.

---

### 5. Response Creation

After processing, the server creates a response containing:
- Status code
- Response headers
- Response body (data or error information)

The response reflects the result of the request processing.

---

### 6. Response Transmission

- The response is sent back to the client
- The connection may be closed or reused
- Network layers deliver the response to the client

---

### 7. Client Handles the Response

The client:
- Reads the response status
- Processes the response data
- Handles errors if present

Once the response is handled, the lifecycle is complete.

---

## Key Characteristics

- Communication follows a request–response pattern
- Each request is handled independently
- The server does not initiate communication
- The lifecycle is stateless by design

---## Handwritten Notes Reference

![notes](notes1.jpg)
![notes](notes2.jpg)

