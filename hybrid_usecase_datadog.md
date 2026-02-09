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
