---
id: shfhe0mo19ida8cn510vso5
title: Request-Response
desc: ''
updated: 1708751295131
created: 1708751256620
---

It is a [[arch.pattern.messaging]].

## Model

- Client sends a request
- Server parses the request: Where does a request begin and end?
- Server processes the request: Example, Deserializing JSON and then processing.
- Server sends a response
- Client parses the response and consume

## Anatomy

- Client and server need to define and agree upon the request/response structure.
- Request/response has a boundary
- Defined by protocol and message format.

## Where is it used?

- Web, HTTP, DNS, SSH.
- Remote Procedure Call (RPC)
- SQL and database protocols
- APIs (REST/SOAP/GraphQL)

## Where it doesn't work well?

- Notification Service
- Chat Applications
- Very Long requests - What if client disconnects?

