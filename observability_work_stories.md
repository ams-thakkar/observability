# Observability & Customer Success Work Stories (STAR Format)

---

## Story 1 – AT&T Central Platform Observability (Splunk vs ELK)

### Situation
At AT&T, I was part of the Office of the CTO Central Platform Engineering team responsible for observability for two newly built, customer-facing microservices platforms: the Knowledge Management system (`att.com/support`) and Search & Discovery (`att.com/search`). These platforms served ~20 million external customers with ~100 million daily visits. The existing monitoring solution was an agent-based APM tool (Wily Introscope), which provided basic JVM metrics but was not designed for modern, distributed microservices architectures.

### Task
My responsibility was to define and lead the design of a modern observability strategy that could scale with high traffic, support distributed tracing, and provide meaningful service-level visibility—while balancing cost, operational overhead, and time-to-production.

### Actions
I started by defining **clear SLIs and SLOs** aligned to customer experience rather than tool capabilities. Based on these requirements, I proposed and led two parallel proofs of concept:
- An in-house **ELK-based solution**
- An enterprise **Splunk-based solution**

I built a comparative analysis covering scalability, operational burden, cost, learning curve, and long-term sustainability. I also partnered with Splunk Solution Architects post-POC to validate production readiness.

### Results
Leadership selected Splunk due to faster time-to-value, lower operational overhead, and ease of adoption. The solution enabled SLO-based alerting, faster detection and recovery, and earned trust across application and platform teams.

### Key SLOs Defined

| SLO Category | Objective |
|-------------|-----------|
| Availability | 99.9% successful request rate for customer-facing APIs |
| Latency (p95) | < 300 ms for search queries |
| Latency (p99) | < 750 ms during peak traffic |
| Error Rate | < 0.1% 5xx errors across core microservices |
| Detection | Mean Time to Detect (MTTD) < 5 minutes |

---

## Story 2 – uShip Hybrid Observability (Datadog + AWS)

### Situation
uShip, an online shipping marketplace for freight and heavy equipment, operated in a hybrid environment with workloads across AWS (EC2, RDS Oracle, Lambda, Kinesis) and on-prem RHEL servers. Fragmented observability impacted reliability of their customer-facing scheduling portal.

### Task
My role was to design a unified observability solution and justify the approach to a VP-level audience, balancing cost, reliability, and hybrid visibility.

### Actions
I led executive discussions focused on **business-critical SLOs** tied to scheduling reliability and demand–supply matching. I proposed a **Datadog-based single-pane-of-glass solution**, led an onsite workshop, and executed a custom POC validating hybrid observability.

### Results
The solution improved confidence in production operations, enabled proactive detection of SLO breaches, and accelerated adoption through clear alignment with business outcomes.

### Key SLOs Defined

| SLO Category | Objective |
|-------------|-----------|
| Scheduling Availability | 99.95% availability of the scheduling portal |
| Latency (p95) | < 400 ms for quote generation and scheduling APIs |
| Data Freshness | < 2 minutes lag in demand–supply matching pipelines |
| Detection | MTTD < 3 minutes for customer-visible failures |

---

## Story 3 – Bell Canada Contact Center Observability

### Situation
Bell Canada operated a large-scale contact center platform with telemetry from RDS SQL Server, Redshift, S3, IVR systems, chatbots, network devices, and agent desktops. While Bell already used Splunk, observability data was fragmented and underutilized.

### Task
I was responsible for designing an observability architecture that unified telemetry into actionable insights focused on customer experience and agent productivity.

### Actions
I worked with stakeholders to define **experience-driven SLOs** and designed a Splunk ingestion strategy on AWS that correlated infrastructure, application, and customer interaction data.

### Results
Bell gained real-time visibility into CX and agent efficiency, enabling faster remediation and better operational decision-making without adding new tooling complexity.

### Key SLOs Defined

| SLO Category | Objective |
|-------------|-----------|
| Call Routing Success | ≥ 99% successful IVR call routing |
| IVR Latency (p95) | < 250 ms response time |
| Chatbot Containment | ≥ 85% interactions resolved without human handoff |
| Agent Desktop Latency (p95) | < 500 ms for core agent workflows |

---

## Story 4 – BMO CardTech OpenTelemetry Adoption

### Situation
At BMO’s CardTech division, teams relied on fragmented tooling (CloudWatch logs and Dynatrace), leading to inconsistency, vendor lock-in, and limited extensibility.

### Task
My goal was to modernize observability using a standardized, vendor-neutral approach that supported future automation and AIOps initiatives.

### Actions
I led adoption of **OpenTelemetry (OTel)** as the standard telemetry layer, enabling consistent collection of traces, metrics, and logs across services while preserving backend flexibility.

### Results
Teams achieved consistent SLO measurement, reduced tooling fragmentation, and created a strong foundation for future AIOps and reliability automation.

### Key SLOs Defined

| SLO Category | Objective |
|-------------|-----------|
| Service Availability | 99.9% availability for card transaction services |
| Latency (p95) | < 200 ms for authorization and validation APIs |
| Error Budget | Error budget consumption used as a release gating signal |

---

## Story 5 – AIOps for MTTR Reduction

### Situation
Engineering teams struggled with high MTTR due to fragmented runbooks, historical tickets, and unstructured operational knowledge.

### Task
I led the design of an in-house **AIOps solution** to improve incident response effectiveness and reduce MTTR at scale.

### Actions
We trained an AI model using SOPs, runbooks, and historical ticket data, leveraging **Claude on Amazon Bedrock** and fine-tuning with CloudWatch logs. The system surfaced contextual recommendations during incidents.

### Results
The solution delivered **5–30% YoY MTTR improvement across 20 teams**, shifting incident response from reactive troubleshooting to AI-assisted decision-making.

### Key SLOs Defined

| SLO Category | Objective |
|-------------|-----------|
| MTTR Reduction | ≥ 20% YoY reduction target |
| Triage Time | < 10 minutes to actionable recommendation |
| Knowledge Retrieval | < 30 seconds to surface relevant SOPs/runbooks |

---
