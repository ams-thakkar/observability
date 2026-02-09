# Story 1 – AT&T Central Platform Observability (Splunk vs ELK)

## Situation

At AT&T, I was part of the Office of the CTO Central Platform Engineering team responsible for observability for two newly built, customer-facing microservices platforms: the Knowledge Management system (`att.com/support`) and Search & Discovery (`att.com/search`). These platforms served ~20 million external customers with ~100 million daily visits. The existing monitoring solution was an agent-based APM tool (Wily Introscope), which provided basic JVM metrics but was not designed for modern, distributed microservices architectures.

## Task
My responsibility was to define and lead the design of a modern observability strategy that could scale with high traffic, support distributed tracing, and provide meaningful service-level visibility—while balancing cost, operational overhead, and time-to-production.

## Actions
I started by defining **clear SLIs and SLOs** aligned to customer experience rather than tool capabilities. Based on these requirements, I proposed and led two parallel proofs of concept:
- An in-house **ELK-based solution**
- An enterprise **Splunk-based solution**

I built a comparative analysis covering scalability, operational burden, cost, learning curve, and long-term sustainability. I partnered closely with Splunk Solution Architects post-POC to validate production readiness.

## Results
Leadership selected Splunk due to faster time-to-value, lower operational overhead, and ease of adoption. The solution enabled SLO-based alerting, faster detection and recovery, and earned trust across application and platform teams.

## Key SLOs

| SLO Category | Objective |
|-------------|-----------|
| Availability | 99.9% successful request rate |
| Latency (p95) | < 300 ms for search queries |
| Latency (p99) | < 750 ms during peak |
| Error Rate | < 0.1% 5xx errors |
| Detection | MTTD < 5 minutes |


## Architecture – Bottom-Up Design
![AT&T Observability Whiteboard – Story 1](https://raw.githubusercontent.com/ams-thakkar/observability/main/observability_whiteboard_story1.png)
