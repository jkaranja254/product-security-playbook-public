# Supply Chain Security Controls

## Purpose

This document outlines practical controls for managing software supply chain risk in a modern cloud-based product.

It focuses on dependencies, build integrity, and external components that can introduce security risk.

---

## Scope

This includes:

- open source dependencies
- internal build artifacts
- third-party services and integrations

It does not cover physical supply chain or hardware-level risks.

---

## Key Risks

Supply chain risk may arise from:

- vulnerable or malicious open source packages
- compromised build environments
- tampering with build artifacts
- excessive trust in third-party services
- lack of visibility into dependencies

---

## Dependency Management

- maintain an inventory of dependencies
- review dependencies based on risk and usage
- monitor for known vulnerabilities
- restrict use of untrusted or unverified packages
- remove unused or unnecessary dependencies

---

## Build Integrity

- ensure builds originate from trusted sources
- restrict modification of build configurations
- maintain separation between build and runtime environments
- verify integrity of build artifacts where possible

---

## Artifact Management

- store build artifacts in controlled repositories
- restrict access to artifact storage
- track versions and changes to artifacts
- avoid manual modification of artifacts after build

---

## Third-Party Services

- evaluate third-party services based on data access and operational dependency
- limit access granted to external services
- review changes in third-party risk posture where relevant
- maintain awareness of critical dependencies

---

## Verification and Monitoring

- monitor dependency updates and changes
- track security advisories relevant to dependencies
- log and review build and deployment activity
- investigate anomalies in build or release processes

---

## Common Failure Points

- lack of visibility into dependency usage
- implicit trust in third-party components
- weak controls around build pipelines
- insufficient review of dependency updates
- failure to remove unused dependencies

---

## Intended Outcome

Effective supply chain controls reduce the risk of introducing vulnerabilities through dependencies, improve confidence in build integrity, and support more resilient software delivery.
