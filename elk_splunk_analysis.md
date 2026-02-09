# Designing and Implementing an ELK stack for support (KANA)

**Summary**

The Knowledge Management System (KANA KMS) supporting att.com/support is a mission-critical Tier-1 platform enabling self-service and assisted support for ~20M external customers, 10K+ support agents, and 60+ content authors. Any degradation in availability, latency, or accuracy directly impacts customer satisfaction, call volumes, and operational cost.

This observability initiative was architected to shift the platform from reactive monitoring to customer-experience assurance, ensuring reliability could be measured, governed, and improved at scale.

The solution was intentionally designed around Service Level Objectives (SLOs) and business outcomes, not tooling, enabling leadership to understand customer impact, not just system health.

**Context & Business Problem Statement**

The current KMS platform relies on a legacy, agent-based APM solution (Wily Introscope) as its primary monitoring tool. While it provided basic JVM-level visibility, it was not designed to support modern, customer-facing, microservice-based architecture that the new KANA KMS system is built on. 

**Application**: KANA Knowledge Management System (KMS)

**Frontend**: att.com/support (public-facing UX)

**Backend**: On-prem application tier + Oracle Database

**User Scale:**

- 45 internal content authors

- 10K internal support agents

- 20M external customers (Mobility + U-Verse)

**Business Criticality**

- Tier-1 customer support dependency

- Direct impact on:

- Call deflection

- Average Handle Time (AHT)

- Customer Satisfaction (CSAT)

- Brand trust and revenue protection

**How Observability Was Orchestrated (High Level)**

1. Observability as a Platform Standard
   - All Spring microservices were required to adopt a shared observability framework
2. 