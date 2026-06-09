```mermaid
graph LR
    AWS --> Physical_Security
    AWS --> Hardware
    AWS --> Hypervisor
    AWS --> RDS_OS_Patching

    Customer --> Guest_OS_Patching
    Customer --> IAM_Configuration
    Customer --> Encryption
    Customer --> Security_Groups

    style AWS fill:#FF9900,color:#000
    style Customer fill:#232F3E,color:#fff
```



