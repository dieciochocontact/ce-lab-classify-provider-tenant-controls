# Lab M8.01 - Classify Controls into Provider vs Tenant Responsibility

## Learning Objectives
- Review AWS Shared Responsibility Model components
- Classify security controls by responsibility (AWS vs customer)
- Identify responsibility for different service models (IaaS, PaaS, SaaS)
- Document security controls and responsibilities for a three-tier architecture

## Files
- `security-inventory.md` - AWS resource inventory
- `responsibility-matrix.md` - Security controls responsibility matrix
- `gap-analysis.md` - Identified security gaps and priorities
- `assessment-report.md` - Comprehensive security assessment report
- `diagram.md` - Visual diagram of shared responsibility model

## Key Findings
- 7 security gaps identified, 2 critical
- EC2 requires highest customer responsibility (IaaS)
- RDS and S3 have shared responsibility (PaaS)
- Main gaps: S3 encryption, RDS encryption, OS patching, MFA
