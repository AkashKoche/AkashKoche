<div align="center">

# Akash Koche
### Cloud & DevOps Engineer · Site Reliability Engineering

[![LinkedIn](https://img.shields.io/badge/LinkedIn-akash--koche-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/akash-koche)
[![GitHub](https://img.shields.io/badge/GitHub-AkashKoche-181717?style=flat&logo=github&logoColor=white)](https://github.com/AkashKoche)
[![Email](https://img.shields.io/badge/Email-koche.akash%40gmail.com-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:koche.akash@gmail.com)
[![Location](https://img.shields.io/badge/Nagpur%2C%20India-available%20for%20remote-1D9E75?style=flat)](#)

</div>

---

Entry-level Cloud & DevOps Engineer focused on **infrastructure automation**, **site reliability**, and **production-grade observability**. I build systems that detect, fix, and recover from failures automatically — reducing MTTR and operational toil through code, not manual intervention.

---

## Featured Projects

### Auto-Remediation Engine — Self-Healing Infrastructure
`FastAPI` `Docker` `Kubernetes` `Prometheus` `Python`

A cloud-native, event-driven system where Prometheus alerts trigger a FastAPI webhook that automatically restarts pods, clears disk, and verifies recovery — without human intervention.

- Implemented **header-based authentication** (X-Auth-Token middleware) to protect remediation endpoints from unauthorized execution
- Deployed on **Kubernetes** with Horizontal Pod Autoscaler, liveness/readiness probes, and NodePort service exposure
- Instrumented with **Prometheus Counters & Histograms** exposed on `/metrics`; visualized via custom Grafana dashboards
- End-to-end tested via an automated Python validation script covering auth, functional, and observability scenarios

> *Complete closed-loop SRE pipeline: detect → authenticate → remediate → verify → log*

---

### Prometheus Cardinality Control — Production Observability Platform
`Prometheus` `Grafana` `Alertmanager` `Docker Compose` `PromQL`

Built to simulate and defend against high-cardinality metric explosions (`user_id`, `request_id` labels) that cause TSDB memory bloat, slow queries, WAL growth, and OOM crashes in production.

- Applied **ingestion-time `metric_relabel_configs`** to drop volatile labels before TSDB storage — the correct fix vs. post-ingestion PromQL filtering
- Built a **synthetic workload generator** with NORMAL, BURST, CARDINALITY\_ATTACK, and MIXED modes for repeatable failure simulation
- Configured **TSDB saturation alerting** on `prometheus_tsdb_head_series` and **recording rules** for pre-aggregated, dashboard-safe metrics
- Delivered Grafana dashboards tracking head series count, WAL growth rate, scrape samples, and alert states

> *Demonstrates Prometheus internals knowledge: TSDB head blocks, WAL, compaction, and PromQL query optimization*

---

### Local Incident Response Assistant — AI-Powered SRE Agent
`LangChain` `Ollama (Llama 3.2)` `Python` `Kubernetes` `kubectl`

An AI-powered Kubernetes SRE agent that autonomously investigates failing pods — fetching status, pulling logs, describing events — then uses LLM reasoning to determine root cause and suggest fixes.

- Built a modular **tool layer** (`get_pods`, `get_logs`, `describe_pod`) wrapping real `kubectl` commands via Python subprocess
- Integrated **LangChain's ReAct agent pattern** with a locally-hosted Llama 3.2 via Ollama for zero-cost, privacy-safe inference
- Simulated **CrashLoopBackOff** scenarios to validate agent reasoning across application-level and Kubernetes-level failure signals
- Designed in safe read-only mode; roadmap includes Prometheus alert integration, RBAC controls, and Slack/PagerDuty notifications

> *Applies AI-Ops reasoning where traditional scripts fail — handles unknown failure patterns through LLM context understanding*

---

### E-Commerce Microservices Platform — AWS Cloud-Native
`Node.js` `React` `Nginx` `Docker` `Terraform` `GitHub Actions` `AWS` `Prometheus`

A production-grade, 3-tier microservices platform on AWS Free Tier demonstrating end-to-end DevOps — from architecture to deployment to observability.

- **Architecture:** React frontend → Nginx API Gateway → Product Service (PostgreSQL) + Cart Service (Redis), fully containerized
- **IaC:** Terraform provisions EC2, RDS, ElastiCache, and ALB; all infrastructure is version-controlled and reproducible
- **CI/CD:** GitHub Actions pipeline covers linting, SAST/DAST security scanning, Docker builds, ECR pushes, and health-gated deployments
- **Observability:** Prometheus + Grafana for real-time metrics; CloudWatch for centralized production logging and alerting

> *Full DevOps lifecycle in one project: architecture · IaC · CI/CD · security scanning · monitoring*

---

### Automated AWS Infrastructure Deployment
`Terraform` `Jenkins` `AWS VPC` `EC2` `IAM`

- Designed modular Terraform scripts for VPC, EC2, Security Groups, and IAM — fully automated via Jenkins pipeline
- Reduced manual provisioning time by **80%**; ensured idempotent, repeatable deployments across environments

---

## Technical Skills

| Domain | Technologies |
|---|---|
| **Cloud** | AWS (EC2, S3, RDS, Lambda, IAM, ECS, ALB, ElastiCache), GCP (GKE, Compute, Cloud Run) |
| **IaC** | Terraform, AWS CloudFormation |
| **Containers & Orchestration** | Kubernetes, Docker, Docker Compose, ECS |
| **CI/CD** | GitHub Actions, Jenkins, GitLab CI, SonarQube, ECR |
| **Observability & SRE** | Prometheus, Grafana, Alertmanager, CloudWatch, ELK Stack, PromQL |
| **Languages** | Python, Bash, FastAPI, Node.js |
| **Databases** | PostgreSQL, MySQL, Redis, DynamoDB |
| **OS** | Ubuntu, CentOS, Red Hat |

---

## Certifications

- **Google IT Support Professional** — System administration, Linux/Windows, networking, cloud fundamentals
- **Google IT Automation with Python Professional** — Python scripting, Git/GitHub, configuration management

---

## Currently

- Building towards **AWS Solutions Architect Associate** certification
- Extending the AI-SRE agent with Prometheus alert integration and controlled auto-remediation
- Open to **Cloud Engineer · DevOps Engineer · SRE** roles — remote or Nagpur-based

---

<div align="center">

*"I don't just monitor systems — I build systems that fix themselves."*

</div>
