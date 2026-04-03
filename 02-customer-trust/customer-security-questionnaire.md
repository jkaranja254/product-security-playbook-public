# Customer Security Questionnaire

## Purpose

This document provides a concise, reusable response framework for common customer security due diligence questions.

It is designed to support consistent, clear, and practical responses without relying on unnecessary technical detail.

---

## How to Use This Document

This document is intended as a baseline response set.

Responses should be adapted based on product scope, customer context, and the sensitivity of the requested information.

Where a control is not implemented or is only partially implemented, the response should be direct and should avoid overstating maturity.

---

## Governance

### Do you maintain security policies and standards?

Yes. Security policies and standards should define baseline expectations for access control, secure development, incident response, logging, and data protection.

### Is security ownership defined?

Yes. Security responsibilities should be assigned across engineering, platform, and security functions to reduce ambiguity and improve accountability.

### Do you perform risk-based security reviews?

Yes. Material changes, high-risk features, and significant architecture decisions should be reviewed based on business and technical risk.

---

## Identity and Access Management

### How is access controlled?

Access should be granted based on role and business need, with emphasis on least privilege and approval-based access for sensitive systems.

### Is multi-factor authentication required?

Privileged and administrative access should require strong authentication, including multi-factor authentication where applicable.

### Are access reviews performed?

Access should be reviewed periodically, especially for privileged roles and high-risk systems.

---

## Data Protection

### How is sensitive data protected?

Sensitive data should be protected through appropriate access restrictions, encryption in transit, and encryption at rest where required by risk or regulatory expectations.

### Is production data restricted?

Access to production data should be limited to authorized personnel with a clear operational need.

### How are secrets handled?

Secrets should be stored and managed through controlled mechanisms rather than hardcoded into source code or configuration files.

---

## Secure Development

### Is security included in the software development lifecycle?

Yes. Security should be integrated into design, code review, dependency management, testing, and release activities.

### Are code changes reviewed?

Yes. Changes should be reviewed before production deployment, with stronger review expectations for high-risk changes.

### Are dependencies monitored?

Dependencies should be reviewed and monitored to reduce the risk introduced by vulnerable or untrusted components.

---

## Logging and Monitoring

### Are security-relevant events logged?

Yes. Administrative activity, authentication events, and other meaningful security events should be logged where appropriate.

### Is monitoring in place?

Yes. Monitoring should support detection of abnormal or high-risk activity in systems and environments that matter most.

### Are audit trails maintained?

Audit trails should be retained for key administrative and operational actions based on risk, operational need, and compliance requirements.

---

## Incident Response

### Do you maintain an incident response process?

Yes. Security incidents should be triaged, investigated, escalated, and resolved through documented procedures.

### Are incidents communicated appropriately?

Incidents with customer impact should be assessed for communication requirements based on contractual, legal, and operational obligations.

### Are roles defined during incident response?

Yes. Incident response should include defined roles for coordination, investigation, communication, and recovery.

---

## Third-Party Risk

### Are vendors and external services reviewed?

Third-party tools and services should be reviewed in proportion to the access, data sensitivity, and operational dependency involved.

### Are software dependencies considered part of supply chain risk?

Yes. Open source packages, build dependencies, and external components should be considered part of supply chain risk management.

### Are third-party changes monitored?

Where relevant, teams should monitor changes in critical vendors, services, and dependencies that could materially affect security or reliability.

---

## Response Principles

Responses to customer security questions should be:
- accurate
- scoped to the product or service in question
- aligned with implemented controls
- reviewed before sharing where the request is sensitive or high impact

---

## Notes

This document is intended as a reusable starting point.

Detailed answers, evidence, or customer-specific responses should be handled separately when needed.
