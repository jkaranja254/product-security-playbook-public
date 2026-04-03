# IAM Architecture

## Purpose

This document outlines a practical identity and access management (IAM) architecture for a modern cloud-based product.

It focuses on how access is structured, controlled, and reviewed across systems, environments, and teams.

---

## Design Goals

The IAM model should:

- enforce least privilege access
- reduce reliance on long-lived credentials
- support strong authentication for sensitive operations
- scale with team and system growth
- maintain clear visibility into access patterns

---

## Core IAM Principles

- access should be role-based, not user-specific
- privileged access should be minimized and controlled
- authentication strength should match risk level
- access decisions should be auditable
- temporary access should be preferred over persistent access

---

## Identity Types

### Human Identities

Used by engineers, operators, and support personnel.

Access should be tied to roles and require strong authentication.

### Service Identities

Used by applications and services.

These identities should be scoped to specific functions and avoid broad permissions.

### External Identities

Used by partners or integrated systems.

Access should be tightly constrained and monitored.

---

## Access Model

### Role-Based Access Control

Access should be granted through roles aligned with job function.

Roles should define:

- permitted actions
- resource scope
- environment boundaries

### Environment Segmentation

Access should be separated across environments such as:

- development
- staging
- production

Production access should be more restricted and require stronger controls.

---

## Authentication Model

- strong authentication should be required for administrative access
- multi-factor authentication should be enforced for high-risk operations
- federated identity should be preferred over local account management where possible

---

## Privileged Access Controls

Privileged access should be:

- limited to a small number of roles
- granted through approval workflows where appropriate
- time-bound when possible
- logged and monitored

Break-glass access should exist but should be tightly controlled and reviewed after use.

---

## Secrets Management

- secrets should not be stored in source code
- secrets should be managed through controlled systems
- access to secrets should be restricted and audited
- rotation should be performed based on risk and exposure

---

## Logging and Monitoring

IAM-related events should be logged, including:

- authentication attempts
- role assignments and changes
- privilege escalations
- access to sensitive systems

Monitoring should focus on detecting abnormal or high-risk behavior.

---

## Common Failure Points

- overly broad roles with excessive permissions
- lack of separation between environments
- long-lived credentials that are not rotated
- insufficient monitoring of privileged activity
- unclear ownership of IAM roles and policies

---

## Intended Outcome

A well-structured IAM architecture reduces the likelihood of unauthorized access, limits the impact of compromised identities, and provides clear visibility into how systems are accessed and managed.

## Related Documents

- [security overview](../01-overview/security-overview.md)
- [shared responsibility model](../01-overview/shared-responsibility-model.md)
- [threat model case study](threat-model-case-study.md)
