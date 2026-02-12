# Akuity Intelligence Runbooks

> [!WARNING]
> ARCHIVED - This project is no longer maintained, and please find examples of runbooks and tasks in [akuity-intelligence-examples](https://github.com/akuity/akuity-intelligence-examples).

This repository contains operational runbooks that guide Akuity Intelligence's automated incident response when it detects degraded ArgoCD Applications or Kubernetes Namespaces. Each runbook follows a structured approach with symptom identification, root cause analysis, and step-by-step remediation procedures.

## Runbook Categories

### ArgoCD Application Issues
Runbooks for health, sync, and deployment issues surfaced through Argo CD:
- **[argocd-app-degraded.md](./argocd/argocd-app-degraded.md)** - Application health degraded with failing resources
- **[argocd-app-out-of-sync.md](./argocd/argocd-app-out-of-sync.md)** - Applications showing out-of-sync status
- **[argocd-app-sync-failure.md](./argocd/argocd-app-sync-failure.md)** - Sync operations failing or timing out

### Infrastructure & Cluster Issues  
Cluster-level infrastructure problems and resource constraints:
- **[pod-pending-scheduling.md](./infra/pod-pending-scheduling.md)** - Pods stuck in pending due to scheduling constraints
- **[pvc-binding-failure.md](./infra/pvc-binding-failure.md)** - Persistent volume claim binding failures
- **[time-drift.md](./infra/time-drift.md)** - Time synchronization issues between cluster nodes

### Network & Connectivity Issues
Network dataplane and service connectivity diagnostics:
- **[cni-networking.md](./networking/cni-networking.md)** - CNI and pod networking problems
- **[service-connectivity.md](./networking/service-connectivity.md)** - Service discovery and connectivity failures

### Pod-Level Problems
Per-pod reliability scenarios and runtime issues:
- **[image-pull-failure.md](./pod-issues/image-pull-failure.md)** - Container image pull failures and registry issues
- **[pod-evictions.md](./pod-issues/pod-evictions.md)** - Pod evictions due to resource pressure
- **[pod-health-issues.md](./pod-issues/pod-health-issues.md)** - Pod health check failures and readiness issues

### Security & Access Control
Access control and policy denials that block workloads:
- **[rbac-denials.md](./security/rbac-denials.md)** - RBAC permission denials and authorization failures
