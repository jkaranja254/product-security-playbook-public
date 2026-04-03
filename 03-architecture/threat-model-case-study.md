# Threat Model Case Study

## Scenario

A cloud-based SaaS application exposes a public API used by web and mobile clients.

The system includes:

- a frontend client
- an API layer
- backend services
- a managed database
- third-party integrations

---

## Scope

This threat model focuses on:

- authentication and authorization flows
- data access paths
- service-to-service communication
- exposure of public endpoints

It does not cover physical infrastructure or endpoint device security.

---

## Assumptions

- the application is internet-facing
- users authenticate through a centralized identity provider
- services communicate over internal networks
- sensitive data is stored in a managed database

---

## Assets and Trust Boundaries

### Key Assets

- customer data
- authentication tokens
- service credentials
- application configuration

### Trust Boundaries

- public client to API boundary
- API to backend service boundary
- service to database boundary
- system to third-party integration boundary

---

## Threats (STRIDE)

### Spoofing

- attackers attempt to impersonate legitimate users or services
- token theft or misuse could allow unauthorized access

### Tampering

- requests or payloads may be modified in transit or at the client level
- improper validation could allow unauthorized changes

### Repudiation

- lack of sufficient logging may prevent tracing of user or administrative actions

### Information Disclosure

- sensitive data may be exposed through misconfigured endpoints or excessive permissions
- logs or error messages may leak internal details

### Denial of Service

- public endpoints may be targeted to degrade availability
- lack of rate limiting could amplify impact

### Elevation of Privilege

- improper role enforcement could allow users or services to gain higher access
- overly broad service permissions could be abused

---

## Key Mitigations

### Authentication and Session Management

- enforce strong authentication for users
- validate tokens at each request boundary
- limit token lifetime and scope

### Authorization Controls

- enforce role-based access checks at the API and service layers
- validate permissions on every request

### Input Validation

- validate and sanitize all external input
- reject malformed or unexpected requests

### Network and Service Controls

- restrict internal service communication
- avoid exposing unnecessary endpoints

### Logging and Monitoring

- log authentication events and administrative actions
- monitor for abnormal access patterns

### Rate Limiting and Protection

- apply rate limiting on public endpoints
- use protective controls against abusive traffic patterns

---

## Residual Risks

- zero-day vulnerabilities in dependencies or platforms
- misconfiguration during rapid deployment or scaling
- insider misuse of authorized access
- gaps in monitoring coverage

---

## Outcome

This threat model highlights key risks across system boundaries and defines practical controls to reduce likelihood and impact.

It supports informed design decisions, improved detection capability, and more resilient system behavior.
