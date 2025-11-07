# SRE Practices (Intermediate)

## Overview

Site Reliability Engineering (SRE) applies software engineering practices to operations: defining SLOs, managing error budgets, and automating toil.

## Core Concepts

- SLI (Service Level Indicator): measurable metric (latency, availability)
- SLO (Service Level Objective): target for SLIs
- SLA (Service Level Agreement): contractual promise
- Error budgets: allowable failure before intervention

## Practices

- Define SLIs/SLOs for critical services
- Automate repetitive operational tasks
- Postmortems with blameless culture
- Capacity planning and incident response runbooks

## Tooling

- Monitoring: Prometheus, Datadog
- Incident management: PagerDuty, OpsGenie
- Runbook automation and playbooks

## Best Practices

- Keep SLOs meaningful and actionable
- Use error budgets to balance innovation and reliability
- Invest in automation to reduce toil

## References

- Google's SRE book
- SLO best practices articles
