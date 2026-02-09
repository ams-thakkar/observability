# Story 3 – Bell Canada Contact Center Observability

## Situation
Bell Canada operated a large-scale contact center platform with telemetry from RDS SQL Server, Redshift, S3, IVR systems, chatbots, network devices, and agent desktops. While Bell already used Splunk, observability data was fragmented and underutilized.

## Task
I was responsible for designing an observability architecture that unified telemetry into actionable insights focused on customer experience and agent productivity.

## Actions
I worked with stakeholders to define **experience-driven SLOs** and designed a Splunk ingestion strategy on AWS that correlated infrastructure, application, and customer interaction data.

## Results
Bell gained real-time visibility into CX and agent efficiency, enabling faster remediation and better operational decision-making without adding new tooling complexity.

## Key SLOs

| SLO Category | Objective |
|-------------|-----------|
| Call Routing Success | ≥ 99% |
| IVR Latency (p95) | < 250 ms |
| Chatbot Containment | ≥ 85% |
| Agent Desktop Latency (p95) | < 500 ms |
