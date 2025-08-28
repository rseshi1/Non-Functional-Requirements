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
  - [ ] Harness/GitHub Actions pipelines updated for new clusters  
  - [ ] Helm values.yaml updated (namespace, cluster-specific values)  
- [ ] **Workload Deployment Testing**  
  - [ ] Dry-run of Helm/kubectl apply in non-prod namespaces  
  - [ ] Validate Deployments, StatefulSets, DaemonSets readiness  
- [ ] **Smoke Tests**  
  - [ ] Route/Ingress availability  
  - [ ] Application health checks, liveness/readiness probes  

---

## 4. Pre-GoLive Validation
- [ ] **Performance & Load Testing**  
  - [ ] Baseline performance vs old cluster  
  - [ ] Stress/load test for peak traffic  
- [ ] **Failover & Rollback Plan**  
  - [ ] Document rollback steps (switch DNS back, restore DB)  
  - [ ] Backup images/configs before final cutover  
- [ ] **Cutover Checklist**  
  - [ ] Freeze deployments during migration window  
  - [ ] Run final DB sync, switch DNS/load balancer  
- [ ] **Stakeholder Sign-Off**  
  - [ ] App owners validate functional/non-functional requirements  
  - [ ] Security team approves compliance checks  

---

## 5. Post-Migration Validation
- [ ] **Monitoring/Alerting**  
  - [ ] Validate all alerts fire as expected  
  - [ ] Confirm dashboards show correct metrics  
- [ ] **Log Verification**  
  - [ ] Ensure logs are flowing to Splunk/ELK  
  - [ ] Check for errors/warnings in pods post-migration  
- [ ] **User Acceptance Testing**  
  - [ ] Confirm business workflows  
  - [ ] Validate integrations (DB, APIs, messaging)  
- [ ] **Operational Handover**  
  - [ ] Update runbooks and on-call docs  
  - [ ] Train support/operations teams  

---

## 6. Day-2 Operations Readiness
- [ ] **Scaling & Reliability**  
  - [ ] HPA/Cluster autoscaler tested  
  - [ ] PodDisruptionBudgets configured  
- [ ] **Backups & DR**  
  - [ ] Velero/Kasten or backup tool configured for namespaces/PVs  
  - [ ] Disaster recovery test run  
- [ ] **Cost & Quota Management**  
  - [ ] Resource quotas applied per project  
  - [ ] Cost monitoring enabled  
- [ ] **Continuous Improvement**  
  - [ ] Collect feedback from migration runbooks  
  - [ ] Update checklist for next batch of apps  
