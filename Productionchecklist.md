# Production Readiness Checklist for OCP Migrations

## 1. Pre-Migration Assessment
- [ ] **Application Inventory**  
  - [ ] List all applications, namespaces, pipelines, databases, and dependencies  
  - [ ] Identify apps with external integrations (DBs, APIs, message queues, etc.)  
- [ ] **Compatibility & Versioning**  
  - [ ] Validate source vs target OCP versions (API deprecations, Operators, Helm charts)  
  - [ ] Confirm workloads use supported APIs (no deprecated APIs)  
- [ ] **Resource Sizing**  
  - [ ] Collect CPU/memory/storage usage (Prometheus metrics)  
  - [ ] Define requests/limits and quotas for target namespaces  
- [ ] **Dependencies Mapping**  
  - [ ] AVI Load Balancer configs, routes/ingress, secrets, configmaps  
  - [ ] Internal/External DB connectivity validated  
- [ ] **Security & Compliance**  
  - [ ] RBAC, NetworkPolicies, PodSecurityPolicies / Pod Security Standards  
  - [ ] Image scanning & registry whitelisting  

---

## 2. Target Cluster Readiness
- [ ] **Cluster Validation**  
  - [ ] Nodes healthy, capacity checks, autoscaling enabled  
  - [ ] Storage classes and PVs provisioned  
- [ ] **Networking**  
  - [ ] Routes/DNS updated, AVI LB mappings tested  
  - [ ] Cluster interconnectivity validated (firewalls, service mesh)  
- [ ] **Monitoring/Logging**  
  - [ ] Prometheus/Grafana dashboards created per namespace  
  - [ ] Centralized logging (Splunk/ELK) integrated  
- [ ] **Secrets & Certificates**  
  - [ ] SSL/TLS certs imported and validated  
  - [ ] KMS/Secret Manager integration tested  

---

## 3. Migration Execution Readiness
- [ ] **Data Migration**  
  - [ ] Database dump/restore or replication strategy defined  
  - [ ] Verify data sync for cutover (no data loss)  
- [ ] **Pipeline/CI-CD Updates**  
  - [ ] Ha
