# Security Responsibility Matrix

## Service Model Classification

| Service | Model | Justification |
|---------|-------|---------------|
| EC2 | IaaS | Customer manages OS, applications, data |
| RDS | PaaS | AWS manages OS, customer manages data and configuration |
| S3 | PaaS | AWS manages infrastructure, customer manages data and access |
| Lambda | FaaS | AWS manages OS and runtime, customer manages code |
| ALB | PaaS | AWS manages infrastructure, customer configures routing |

## Network Security

| Control | AWS | Customer | Status |
|---------|-----|----------|--------|
| VPC isolation | ✅ Hypervisor isolation | ✅ VPC configuration, subnets | ✅ Configured |
| Security groups | ✅ Infrastructure | ✅ Rules configuration | ⚠️ Review needed |
| NACLs | ✅ Infrastructure | ✅ Rules configuration | ✅ Configured |
| DDoS protection | ✅ AWS Shield Standard | ✅ Enable Shield Advanced (optional) | ❌ Not enabled |

## Compute Security (EC2)

| Control | AWS | Customer | Status |
|---------|-----|----------|--------|
| Host OS | ✅ Patching and security | ❌ None | ✅ AWS Managed |
| Guest OS | ❌ None | ✅ Patching, hardening, antivirus | ⚠️ TODO |
| Application security | ❌ None | ✅ Secure coding, dependencies | ⚠️ TODO |
| IAM role | ✅ Infrastructure | ✅ Policy configuration | ✅ Configured |
| Instance isolation | ✅ Hypervisor | ❌ None | ✅ AWS Managed |

## Database Security (RDS)

| Control | AWS | Customer | Status |
|---------|-----|----------|--------|
| Database OS | ✅ OS patching | ❌ None | ✅ AWS Managed |
| Database engine | ✅ Patching with maintenance window | ✅ Schedule maintenance, test | ✅ Configured |
| Encryption at rest | ✅ KMS infrastructure | ✅ Enable encryption, manage keys | ⚠️ TODO |
| Network access | ✅ Infrastructure | ✅ Security groups, subnet placement | ✅ Private subnet |
| Backup | ✅ Automated backups | ✅ Configure retention, test restore | ⚠️ Test restore |

## Data Security (S3)

| Control | AWS | Customer | Status |
|---------|-----|----------|--------|
| Storage infrastructure | ✅ Redundancy, durability | ❌ None | ✅ AWS Managed |
| Encryption at rest | ✅ KMS infrastructure | ✅ Enable encryption | ⚠️ TODO |
| Bucket policies | ✅ Infrastructure | ✅ Configure policies | ⚠️ Review needed |
| Public access | ✅ Infrastructure | ✅ Block Public Access setting | ⚠️ TODO |
| Versioning | ✅ Infrastructure | ✅ Enable versioning | ❌ Not enabled |

## Identity & Access (IAM)

| Control | AWS | Customer | Status |
|---------|-----|----------|--------|
| MFA enforcement | ✅ Infrastructure | ✅ Enable MFA for all users | ⚠️ TODO |
| Password policy | ✅ Infrastructure | ✅ Configure password policy | ⚠️ TODO |
| Least privilege | ✅ Infrastructure | ✅ Review and restrict IAM policies | ⚠️ TODO |