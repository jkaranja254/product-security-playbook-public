# Shared Responsibility Model

## Purpose

This document defines how security responsibilities are distributed across engineering, security, and platform teams in a modern cloud-based product environment.

It clarifies ownership to reduce ambiguity, improve accountability, and ensure security controls are consistently applied.

---

## Core Principle

Security is a shared responsibility.

No single team owns security end-to-end. Instead, ownership is distributed based on system boundaries, roles, and operational control.

---

## Responsibility Breakdown

### Application Layer

Owned primarily by engineering teams.

Responsibilities include:

- secure coding practices
- input validation and error handling
- authentication and authorization logic
- dependency management
- application-level logging

### Platform and Infrastructure

Owned by platform or infrastructure teams.

Responsibilities include:

- cloud resource configuration
- network controls and segmentation
- base image and runtime hardening
- infrastructure monitoring
- secrets management at the platform level

### Security Team

Provides guidance, standards, and oversight.

Responsibilities include:

- defining security policies and standards
- supporting threat modeling and design reviews
- monitoring for systemic risks
- coordinating incident response
- enabling security tooling and visibility

---

## Cross-Team Responsibilities

Some responsibilities are shared and require coordination:

- access management and role design
- logging and monitoring coverage
- incident response execution
- vulnerability remediation prioritization
- change management and release controls

---

## Common Failure Points

- unclear ownership of specific controls
- over-reliance on the security team for implementation
- gaps between infrastructure and application responsibilities
- inconsistent enforcement of standards
- lack of visibility into shared systems

---

## Operating Model

Effective shared responsibility requires:

- clearly documented ownership boundaries
- standard definitions for roles and responsibilities
- regular cross-team communication
- visibility into system behavior and changes
- escalation paths for security issues

---

## Intended Outcome

A well-defined shared responsibility model reduces confusion, improves execution, and ensures security is consistently applied across the product lifecycle.
