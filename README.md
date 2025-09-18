# Akuity Intelligence Runbooks

This repository contains the example operational runbooks that Akuity Intelligence incident triggers when it detects degraded ArgoCD/Namespace resources. The documents are written for on-call responders so they can quickly triage issues, collaborate with engineers, and restore service health.

## Audience and Scope
- Primary users are on-call SREs and platform engineers responding to degraded resource incidents raised by Akuity Intelligence.
- Runbooks assume access to Akuity-managed Argo CD instances, Kubernetes clusters, and observability tooling (logs, metrics, events).
- Each document highlights the actions that an automated assistant can safely take versus items that require explicit human approval.

## How to Use These Runbooks
- Start with the **General** section at the top of each runbook. It captures mandatory triage steps, Slack communication expectations, and the reminder to avoid making unauthorised changes.
- Follow the remaining sections sequentially. They are organised by symptom → root cause hypotheses → validation steps → remediation guidance.
- Update the `"PLEASE REPLACE"` placeholder in Slack callouts with the production incident channel that your team uses before automating notifications.
- Modify based on the specific needs, and then import or copy&paste to the Akuity Intelligence runbook configuration.

## Repository Layout
- `argocd/` – Health, sync, and deployment issues surfaced through Argo CD (e.g. degraded health, out-of-sync apps, sync failures).
- `infra/` – Cluster-level infrastructure signals such as pending pods, PVC binding errors, and time drift between nodes.
- `networking/` – Network dataplane and service connectivity diagnostics.
- `pod-issues/` – Per-pod reliability scenarios including image pull failures, pod evictions, general health anomalies, etc.
- `security/` – Access control and policy denials that block workloads.

For questions or missing scenarios, feel free to submit example runbooks based on your senarios, reach out to Akuity or file an issue in this repository.
