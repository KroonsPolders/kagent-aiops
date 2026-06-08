# Agentic AI for Kubernetes Operations (AIOps)

## Overview

This project demonstrates an Agentic AI-powered Kubernetes Operations platform built using:

- Kagent
- Ollama
- Llama 3.2
- Kubernetes (Kind)
- Helm

The platform enables AI agents to:

- Investigate Kubernetes failures
- Perform root cause analysis
- Collaborate with specialized agents
- Recommend remediation actions
- Support Human-in-the-Loop approval workflows

---

## Architecture

```text
User
 │
 ▼
Cluster Remediator Agent
 │
 ├── k8s-agent
 ├── observability-agent
 ├── helm-agent
 └── promql-agent
          │
          ▼
    Kubernetes Cluster
          │
          ▼
   Ollama (Llama 3.2)
```

---

## Agentic AI Capabilities

- Goal-oriented reasoning
- Tool usage
- Multi-agent collaboration
- Root cause analysis
- Human approval workflow
- Kubernetes diagnostics

---

## Demo Scenario

Create a failing pod:

```bash
kubectl run crashpod \
  --image=busybox \
  --restart=Never \
  -- sh -c "exit 1"
```

Ask the Cluster Remediator:

```text
Investigate crashpod
```

Agent workflow:

```text
Investigate
↓
Analyze
↓
Identify Root Cause
↓
Recommend Fix
↓
Wait for Approval
```

---

## Technology Stack

| Component | Purpose |
|------------|----------|
| Kubernetes | Runtime |
| Kind | Local Cluster |
| Kagent | Agent Framework |
| Ollama | Local LLM |
| Llama 3.2 | Model |
| Helm | Deployment |

---

## Future Enhancements

- Automated remediation
- Slack integration
- Jira ticket creation
- Incident response workflows
- SRE automation
