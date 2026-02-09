# Story 2 – uShip Hybrid Observability (Datadog + AWS)

## Situation
uShip, an online shipping marketplace for freight and heavy equipment, operated in a hybrid environment with workloads across AWS (EC2, RDS Oracle, Lambda, Kinesis) and on-prem RHEL servers. Fragmented observability impacted reliability of their customer-facing scheduling portal.

## Task
My role was to design a unified observability solution and justify the approach to a VP-level audience, balancing cost, reliability, and hybrid visibility.

## Actions
I led executive discussions focused on **business-critical SLOs** tied to scheduling reliability and demand–supply matching. I proposed a **Datadog-based single-pane-of-glass solution**, led an onsite workshop, and executed a custom POC validating hybrid observability.

## Results
The solution improved confidence in production operations, enabled proactive detection of SLO breaches, and accelerated adoption through clear alignment with business outcomes.

## Key SLOs

| SLO Category | Objective |
|-------------|-----------|
| Scheduling Availability | 99.95% |
| Latency (p95) | < 400 ms |
| Data Freshness | < 2 minutes lag |
| Detection | MTTD < 3 minutes |

## Architecture – Bottom-Up Design
![AT&T Observability Whiteboard – Story 1](https://raw.githubusercontent.com/ams-thakkar/observability/main/observability_whiteboard_story2.png)

## Decision Tradeoff – Datadog vs CloudWatch
The following tradeoffs were evaluated to determine the best observability platform for a **hybrid (AWS + on-prem)** environment supporting a customer-facing scheduling portal:

| Dimension | CloudWatch (AWS-Native) | Datadog (SaaS Observability) |
|---------|-------------------------|------------------------------|
| Environment Coverage | Strong for AWS services | Strong across AWS + on-prem |
| Time to Value | Fast for AWS workloads | Fast across hybrid workloads |
| Operational Overhead | Low (fully managed) | Low (SaaS-managed) |
| Cross-Environment Correlation | Limited without custom glue | Native, out-of-the-box |
| Executive Visibility | Good (AWS-centric) | Strong (unified dashboards) |
| Cost Model | Usage-based | License + usage |
| Customization | Medium | Medium |
| Vendor Lock-in | AWS-centric | Third-party dependency |

**Decision Rationale:**  
CloudWatch provided excellent AWS-native visibility, but Datadog delivered a true **single pane of glass** across cloud and on-prem systems. Given the customer’s hybrid architecture and customer-facing SLOs, reducing cognitive load and improving cross-environment correlation outweighed the additional licensing cost.
