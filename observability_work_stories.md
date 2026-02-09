# Principal-Level Observability & Customer Success Stories
**Focus:** Scale, impact, cross-org ownership, and durable mechanisms  
**Target Role:** Principal Observability Customer Success Specialist (AWS)

---

## Story 1 – AT&T Central Platform Observability (Splunk vs ELK)
**Principal Theme:** Enterprise platform strategy, SLO-driven decisioning, ownership without authority

### Situation (Scale & Context)
At AT&T, I was part of the Office of the CTO Central Platform Engineering team responsible for observability for two tier-0, customer-facing microservices platforms: Knowledge Management (`att.com/support`) and Search & Discovery (`att.com/search`). These platforms served ~20M customers and ~100M daily visits. The incumbent agent-based APM solution (Wily Introscope) provided JVM-level metrics but could not support distributed, customer-facing microservices at scale.

### Task (Principal Scope)
Define an **enterprise observability strategy** anchored on customer outcomes, influence Director- and VP-level leadership, and balance cost, time-to-value, and long-term operational ownership—without direct authority over application teams.

### Actions (Mechanisms & Leverage)
- Defined **customer-aligned SLIs and SLOs** before evaluating tools
- Ran **parallel POCs** for an in-house ELK stack and an enterprise Splunk solution
- Built a decision framework evaluating scalability, SLO operability, app-team adoption, and long-term operational toil
- Partnered with Splunk Solution Architects post-POC to validate production readiness and operating models

### Key SLOs

| SLO Category | Objective |
|---|---|
| Availability | 99.9% successful request rate |
| Latency (p95) | < 300 ms |
| Latency (p99) | < 750 ms (peak) |
| Error Rate | < 0.1% 5xx |
| Detection (MTTD) | < 5 minutes |

### Results (Enterprise Impact)
Splunk was selected to minimize long-term platform toil while enabling rapid SLO adoption. Outcomes included faster detection and recovery, consistent SLO dashboards across tier-0 systems, and increased trust from application teams and executive leadership.

### Stakeholders
**Internal:** CTO org (Directors/VPs), Platform Engineering, App teams, SRE/Ops  
**External:** Splunk Solution Architects, Splunk account leadership

---

## Story 2 – uShip Hybrid Observability (Datadog vs CloudWatch)
**Principal Theme:** Executive influence, hybrid strategy, business-aligned adoption

### Situation (Scale & Context)
uShip, a high-volume online shipping marketplace, operated a hybrid environment with workloads across AWS (EC2, RDS Oracle, Lambda, Kinesis) and on-prem RHEL systems. Fragmented observability impacted reliability of the customer-facing scheduling portal.

### Task (Principal Scope)
Drive an **exec-level observability decision** that reduced hybrid blind spots and protected customer-facing reliability SLOs.

### Actions (Influence & Framing)
- Reframed discussions around **business SLOs**, not tooling
- Evaluated CloudWatch vs Datadog against hybrid correlation and SLO coverage
- Led an executive workshop and a custom hybrid POC

### Key SLOs

| SLO Category | Objective |
|---|---|
| Scheduling Availability | 99.95% |
| API Latency (p95) | < 400 ms |
| Data Freshness | < 2 minutes |
| Detection (MTTD) | < 3 minutes |

### Results (Business Impact)
Datadog was selected to provide a single pane of glass across hybrid systems, enabling proactive SLO breach detection and restoring executive confidence in operational readiness.

### Stakeholders
**Internal:** AWS account team, AWS Partner team
**External:** SHI architects, uShip VP Engineering/Technology, App teams, Ops team

---

## Story 3 – Bell Canada Contact Center Observability (CX-Driven)
**Principal Theme:** CX-first observability, multi-domain correlation

### Situation (Scale & Context)
Bell Canada operated a large contact center platform with telemetry across IVR systems, chatbots, agent desktops, network infrastructure, and AWS data stores (RDS, Redshift, S3). Observability existed but was disconnected from customer experience.

### Task (Principal Scope)
Redefine observability around **customer experience SLOs** and align engineering, operations, and business stakeholders.

### Actions (Systems Thinking)
- Defined CX-driven SLOs across the end-to-end customer journey
- Designed correlation strategy using call/session IDs
- Unified infrastructure, application, and CX telemetry using existing Splunk investments

### Key SLOs

| SLO Category | Objective |
|---|---|
| Call Routing Success | ≥ 99% |
| IVR Latency (p95) | < 250 ms |
| Chatbot Containment | ≥ 85% |
| Agent Desktop Latency (p95) | < 500 ms |

### Results (Organizational Impact)
Shifted operations from system health monitoring to **end-to-end CX visibility**, enabling faster remediation of customer-impacting issues without introducing additional tooling sprawl.

### Stakeholders
**Internal:** AWS account team, Technical Account Manager (TAM)
**External:** Bell contact center engineering, Network Ops, CX/business leaders

---

## Story 4 – BMO CardTech OpenTelemetry Adoption
**Principal Theme:** Standardization, future-proofing, ecosystem leverage

### Situation (Scale & Context)
BMO CardTech teams used fragmented observability tooling (CloudWatch + Dynatrace), leading to inconsistent telemetry and vendor lock-in.

### Task (Principal Scope)
Establish a **durable observability foundation** that scaled across teams and supported future AIOps and reliability initiatives.

### Actions (Strategic Enablement)
- Introduced **OpenTelemetry** as the standard telemetry abstraction
- Defined common schemas for metrics, traces, and logs
- Enabled backend independence while preserving consistent SLO measurement

### Key SLOs

| SLO Category | Objective |
|---|---|
| Service Availability | 99.9% |
| API Latency (p95) | < 200 ms |
| Error Budget Policy | Error budget burn used as release gate |

### Results (Durable Value)
Reduced vendor lock-in, improved interoperability, and positioned the organization for advanced analytics and AIOps.

### Stakeholders
**Internal:**  AWS Account Team, AWS BD Specialist
**External:** CardTech app teams, Sr. Principal of Card Tech Platform

---

## Story 5 – AIOps for MTTR Reduction
**Principal Theme:** Automation at scale, measurable outcomes

### Situation (Scale & Context)
High MTTR across multiple teams due to fragmented operational knowledge (runbooks, tickets, logs).

### Task (Principal Scope)
Design and roll out an **AIOps capability** that reduced MTTR while maintaining trust and safety.

### Actions
- Built AI-assisted incident response using **Claude on Amazon Bedrock**
- Grounded outputs in SOPs, historical tickets, and CloudWatch logs
- Implemented confidence scoring and feedback loops

### Key SLOs

| SLO Category | Objective |
|---|---|
| MTTR Reduction | ≥ 20% YoY |
| Incident Triage | < 10 minutes |
| Knowledge Retrieval | < 30 seconds |

### Results
Delivered **5–30% YoY MTTR reduction across 20 teams**, shifting operations to AI-assisted decisioning.

### Stakeholders
**Internal:** 20+ app teams, Principal Engineer, Program Managers  

---

## Story 6 – Principal Architect Impact at Scale: Bank of Montreal (BMO)
**Principal Theme:** Multi-threaded ownership, executive influence, material revenue impact

### Situation (Scale & Context)
BMO was already the **largest AWS customer in Canada by consumption**, with multiple high-impact migration initiatives running in parallel across data, end-user computing, and infrastructure.

### Task (Principal Scope)
Act as a **force multiplier** across the account by driving multiple parallel migrations, aligning AWS service teams, ProServe, partners, and account leadership, and translating technical initiatives into ROI-driven executive decisions.

---

### Workstream 1: Teradata → Amazon Redshift

#### Actions
- Coordinated with **AWS Redshift service team leadership**
- Led **ROI/TCO presentations** with BMO Directors and AWS Account team
- Scoped and demoed a production-grade POC with **AWS ProServe**
- Onboarded ProServe delivery teams and removed execution blockers

#### SLOs / Success Metrics

| Category | Objective |
|---|---|
| Commercial Impact | >$800K AWS consumption over 3 years |
| Migration Confidence | POC meets performance & cost benchmarks |
| Time to Commitment | Executive commitment post-POC |

#### Results
BMO committed to the Redshift migration, unlocking **>$800K in projected AWS consumption** and establishing a strategic data modernization path.

---

### Workstream 2: Citrix → AWS WorkSpaces

#### Actions
- Led discussions with **BMO senior SRE stakeholders**
- Engaged AWS EUC specialists for demos and workshops
- Mentored a **L6 Solutions Architect** to scale internal execution
- Led Citrix-on-AWS vs WorkSpaces analysis and cost modeling

#### SLOs / Success Metrics

| Category | Objective |
|---|---|
| Pilot Scope | 30 WorkSpaces |
| Contract Leverage | Reduce Citrix renewal from 3 years → 1 year |
| Enablement | L6 SA independently driving follow-ups |

#### Results
BMO committed to a **30-user WorkSpaces pilot** and limited their Citrix renewal, creating strategic optionality for EUC modernization.

---

### Workstream 3: Windows Server Migration & EDP Modeling

#### Actions
- Built cost models for migrating **1,400+ Windows servers** to EC2
- Designed RI + On-Demand + SPOT strategy
- Integrated models into **AWS Enterprise Discount Program (EDP)** negotiations

#### SLOs / Success Metrics

| Category | Objective |
|---|---|
| Migration Scope | 1,400+ servers |
| Cost Optimization | Optimized RI/OD/SPOT mix |
| GTM Alignment | Included in EDP |

#### Results
The analysis directly supported **BMO signing an $11M AWS EDP**.

---

### Overall Results & Recognition
- Enabled multiple parallel migrations across data, EUC, and infrastructure
- Influenced Director-level BMO stakeholders
- Drove **>$800K in committed workload consumption**
- Contributed materially to **$11M AWS EDP signing**
- Mentored and up-leveled a senior SA
- Awarded the **#OneTeam Award** by **AWS VP of Sales Greg Pearson** at AWS SKO, alongside the AWS Account team

### Stakeholders
**Internal (AWS):** AWS Account team, Redshift leadership, EUC specialists, AWS ProServe, Partner team, other SAs, Customer Success  
**External (BMO):** Tech Directors, Senior SREs, Data & App teams, Business stakeholders

---

## Why This Signals Principal (L7)
- Explicit **SLO ownership** tied to business and CX outcomes  
- **Account-level and enterprise-scale impact**  
- Multi-threaded execution with **measurable revenue influence**  
- Demonstrated **leverage through others**  
- External recognition reinforcing **Earn Trust and Deliver Results**
