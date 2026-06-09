# AWS Shared Responsibility Assessment Report

## Executive Summary
This report documents the security responsibilities for a three-tier application running on AWS. We identified 7 gaps that require attention, 2 of them critical.

## Architecture Overview
- Web tier: ALB + EC2 (public subnet)
- App tier: EC2 with Node.js (private subnet)
- Data tier: RDS PostgreSQL (private subnet)

## Service Model Classification
- EC2: IaaS (high customer responsibility)
- RDS: PaaS (medium customer responsibility)
- S3: PaaS (medium customer responsibility)
- ALB: PaaS (low customer responsibility)
- Lambda: FaaS (low customer responsibility)

## Responsibility Matrix
See responsibility-matrix.md for the complete control mapping.

## Gap Analysis
See gap-analysis.md for the complete gap analysis.

## Recommendations
1. Enable S3 default encryption (1 day)
2. Deploy AWS Systems Manager for patch management (3 days)
3. Conduct security group audit (2 days)
4. Migrate RDS to encrypted instance (1 week)
5. Enable S3 versioning on all buckets (1 day)
6. Enable MFA for all IAM users (1 day)
7. Configure IAM password policy (1 hour)

## Conclusion
A clear understanding of the shared responsibility model is critical to avoid security gaps. The 7 identified controls must be implemented within the next 2 weeks to achieve a minimum security baseline.