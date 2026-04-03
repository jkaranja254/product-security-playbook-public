# CI/CD Security Controls

## Purpose

This document outlines practical security controls that should be applied across a CI/CD pipeline for a modern cloud-based product.

It focuses on preventing, detecting, and limiting risk during code integration, build, and deployment.

---

## Pipeline Security Goals

The CI/CD pipeline should:

- prevent unauthorized or unreviewed code from reaching production
- detect common security issues early in the development lifecycle
- protect build and deployment processes from tampering
- maintain traceability for changes and releases

---

## Control Areas by Stage

### Source Control

- enforce branch protection on main branches
- require pull requests for changes
- require code reviews before merge
- restrict direct commits to protected branches
- maintain audit history of changes

---

### Build Stage

- ensure builds are reproducible where possible
- restrict who can modify build configurations
- use controlled build environments
- prevent use of untrusted build scripts

---

### Dependency Management

- monitor dependencies for known vulnerabilities
- restrict use of untrusted or unverified packages
- maintain visibility into third-party components
- review dependency updates for risk

---

### Secrets Handling

- do not store secrets in source code
- inject secrets securely at runtime
- restrict access to secrets in pipelines
- rotate secrets based on risk and exposure

---

### Testing and Validation

- integrate security checks into the pipeline where practical
- validate configuration and infrastructure definitions
- enforce basic quality and security gates before deployment

---

### Deployment Controls

- require approval for production deployments where appropriate
- restrict who can deploy to production
- log all deployment actions
- ensure deployments are traceable to code changes

---

## Minimum Required Controls

At a minimum, pipelines should enforce:

- pull request reviews before merge
- restricted access to production deployment
- secure handling of secrets
- visibility into dependency risk
- logging of key pipeline actions

---

## Common Failure Points

- overly permissive access to pipelines
- hardcoded secrets in repositories
- lack of review for critical changes
- insufficient visibility into build processes
- weak separation between environments

---

## Intended Outcome

A secure CI/CD pipeline reduces the risk of introducing vulnerabilities, limits the impact of compromised workflows, and supports reliable and auditable software delivery.

## Related Documents

- [supply chain controls](supply-chain-controls.md)
- [threat model case study](../03-architecture/threat-model-case-study.md)
