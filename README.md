# Highly Available 3-Tier Web Application on AWS

A hands-on AWS project to design, deploy and operate a web application that stays online even if one Availability Zone fails.

---

## Goal

Build a secure, highly available, monitored web application on AWS, step by step, and document every phase with screenshots and lessons learned.

## Architecture

```
Users
  |
  v
Application Load Balancer        <- Tier 1: presentation (public subnets)
  |
  +--> EC2 web server (AZ A)     <- Tier 2: application (private subnets)
  +--> EC2 web server (AZ B)        managed by an Auto Scaling group
          |
          v
   RDS database (Multi-AZ)       <- Tier 3: data (private subnets)
   Primary (AZ A) + Standby (AZ B)

Supporting services: S3 (files and backups), CloudWatch (alarms), SNS (email alerts), IAM (access control)
```

## AWS services used

| Area | Services |
|---|---|
| Networking | VPC, public/private subnets, route tables, security groups, NACLs |
| Compute | EC2 (Linux), Auto Scaling group, Application Load Balancer |
| Data | RDS (Multi-AZ), S3 |
| Monitoring | CloudWatch alarms, SNS email notifications |
| Security | IAM roles and policies, MFA, security groups |

## Build phases

1. **Foundation:** MFA, budget alert, IAM roles and policies
2. **Compute:** Linux EC2 web server
3. **Scaling:** Load balancer and Auto Scaling group across 2 AZs
4. **Network:** Custom VPC with public and private subnets
5. **Data:** RDS Multi-AZ database and SQL practice
6. **Storage:** S3 bucket for static files and backups
7. **Monitoring:** CloudWatch alarm with SNS email alert
8. **Edge (optional):** CloudFront in front of the load balancer

---

## Phase 1: Foundation

*What I did:*

*Screenshots:*

*What I learned:*

## Phase 2: Compute

*What I did:*

*Screenshots:*

*What I learned:*

## Phase 3: Scaling

*What I did:*

*Screenshots:*

*What I learned:*

## Phase 4: Network

*What I did:*

*Screenshots:*

*What I learned:*

## Phase 5: Data

*What I did:*

*Screenshots:*

*SQL practice:*

*What I learned:*

## Phase 6: Storage

*What I did:*

*Screenshots:*

*What I learned:*

## Phase 7: Monitoring

*What I did:*

*Screenshots:*

*What I learned:*

---

## Troubleshooting log

Real problems I hit and how I fixed them.

| Symptom | Cause | Fix |
|---|---|---|
| | | |

## Cost control

- Budget alert set before building anything.
- Resources are stopped or deleted after each lab session.
- Costly items (load balancer, Multi-AZ RDS, NAT gateway) are only run while testing.

## Well-Architected pillars

| Pillar | How this project addresses it |
|---|---|
| Security | Private subnets, security groups, IAM roles, MFA |
| Reliability | Multi-AZ design, Auto Scaling, health checks |
| Performance | Load balancing across servers |
| Cost optimization | Right-sized instances, teardown after labs |
| Operational excellence | CloudWatch alarms, documented runbooks |

## Future improvements

- Recreate the infrastructure with Terraform
- Add CloudFront and a WAF rule
- Add automated backups and a documented disaster recovery plan

## Author

Shrishti Gupta

*Note: no credentials, access keys or account IDs are stored in this repository.*
