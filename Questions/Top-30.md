# 🚀 DevOps Interview Questions (Advanced + Real-World Scenarios) – Top 30

## 📌 Overview
This guide contains **30 advanced DevOps interview questions with detailed answers**, focusing on:

- Real-world production debugging
- System design thinking
- Root cause analysis
- Practical tools: AWS, Kubernetes, Terraform, CI/CD

---

## 🧠 1. Everything looks healthy, but users are getting errors. Why?

### Explanation:
Infrastructure health does not guarantee application health.

### Possible causes:
- Partial failures (some pods failing)
- Dependency issues (DB/API)
- Load balancer misrouting
- Cache inconsistency (CloudFront / Redis)
- Timeout/retry misconfiguration

### Debug approach:
- Check application logs
- Trace full request flow
- Compare success vs failure rate

### Tools:
- Kubernetes (`kubectl logs`)
- AWS CloudWatch
- Prometheus + Grafana
- AWS X-Ray

---

## 🧠 2. No code or infra change, but production fails. What do you check?

### Common hidden causes:
- Expired TLS certificates (ACM)
- Expired tokens (IAM, OAuth)
- External API changes
- DNS issues
- Secret rotation

### Debug:
- Validate certificates
- Check secrets
- Inspect logs

### Tools:
- AWS ACM
- Route53
- Secrets Manager

---

## 🧠 3. System works in staging but fails in production. Why?

### Causes:
- Data volume difference
- Config differences
- IAM permissions
- Network restrictions

### Debug:
- Compare configs
- Validate environment variables
- Check scaling behavior

### Tools:
- Terraform
- Kubernetes ConfigMaps/Secrets
- AWS IAM

---

## 🧠 4. High CPU usage but low traffic. Why?

### Causes:
- Infinite loop
- Background jobs
- Memory leak causing CPU spikes

### Debug:
- Inspect container processes
- Analyze CPU trends

### Tools:
- `kubectl top pod`
- Prometheus

---

## 🧠 5. Latency increased but CPU/memory normal. Why?

### Causes:
- Network latency
- Slow DB queries
- External API delays

### Debug:
- Trace request path
- Check DB metrics

### Tools:
- AWS X-Ray
- Grafana

---

## 🧠 6. Autoscaling triggered, but performance didn’t improve. Why?

### Causes:
- DB bottleneck
- App not horizontally scalable
- Cold starts

### Tools:
- Kubernetes HPA
- AWS Auto Scaling
- RDS metrics

---

## 🧠 7. Traffic drops to zero but systems are running. Why?

### Causes:
- DNS issue
- Load balancer failure
- TLS error

### Tools:
- Route53
- AWS ALB
- `dig`, `curl`

---

## 🧠 8. Intermittent failures under load. Why?

### Causes:
- Race conditions
- Connection pool exhaustion
- Rate limiting

---

## 🧠 9. CI/CD pipeline suddenly failing. Why?

### Causes:
- Dependency updates
- Token expiry
- Environment changes

### Tools:
- GitHub Actions / Jenkins
- Docker

---

## 🧠 10. Deployment successful but new version not visible. Why?

### Causes:
- CDN cache (CloudFront)
- Load balancer routing
- Canary deployment

---

## 🧠 11. System passes health checks but fails real traffic. Why?

### Cause:
Health checks are too basic.

### Fix:
- Improve readiness probes
- Add synthetic monitoring

---

## 🧠 12. Logs show no errors but users complain. Why?

### Causes:
- Missing logs
- Silent failures
- Frontend issues

---

## 🧠 13. Disk usage suddenly spikes. Why?

### Causes:
- Log growth
- Temp files

---

## 🧠 14. Memory usage increases over time. Why?

### Cause:
Memory leak

---

## 🧠 15. API works locally but fails in cloud. Why?

### Causes:
- IAM issues
- Networking
- Environment variables

---

## 🧠 16. Requests timing out randomly. Why?

### Causes:
- Load balancer timeout
- Backend slowness

---

## 🧠 17. Rolling deployment causes downtime. Why?

### Causes:
- No readiness probe
- Low replica count

---

## 🧠 18. Cache causing inconsistent data. Why?

### Causes:
- Cache invalidation issue
- TTL mismatch

---

## 🧠 19. High error rate after scaling. Why?

### Causes:
- Cold starts
- Dependency overload

---

## 🧠 20. Database CPU high but app CPU low. Why?

### Cause:
Database bottleneck

---

## 🧠 21. AWS cost suddenly spikes. Why?

### Causes:
- Autoscaling surge
- Data transfer cost
- Misconfigured resources

### Tools:
- AWS Cost Explorer
- CloudWatch

---

## 🧠 22. Service works internally but not externally. Why?

### Causes:
- Security groups
- NACL
- Load balancer config

---

## 🧠 23. Config changes not applied. Why?

### Cause:
Pods not restarted

---

## 🧠 24. TLS errors suddenly appear. Why?

### Causes:
- Certificate expired
- Misconfiguration

---

## 🧠 25. Dependency failure causes cascade failure. Why?

### Cause:
No circuit breaker

---

## 🧠 26. Slow startup after deployment. Why?

### Causes:
- Large Docker images
- Dependency loading

---

## 🧠 27. High retries but low success. Why?

### Causes:
- Bad retry logic
- Downstream failure

---

## 🧠 28. System works but user experience is poor. Why?

### Causes:
- Latency
- Partial failures

---

## 🧠 29. Monitoring shows normal but issues exist. Why?

### Causes:
- Wrong metrics
- Missing observability

---

## 🧠 30. How do you debug an unknown production issue?

### Structured approach:

1. Identify scope (who is affected)
2. Check logs and metrics
3. Trace request flow
4. Isolate failing component
5. Rollback if needed

### Tools:
- Kubernetes (`kubectl`)
- AWS CloudWatch
- Prometheus / Grafana
- CI/CD logs

---

## 📌 Conclusion

Advanced DevOps is about:
- Debugging complex systems
- Understanding dependencies
- Thinking beyond tools

---

## ⭐ Support

- Star ⭐ the repo  
- Share with others  
- Follow for more DevOps content  
