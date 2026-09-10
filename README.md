# AWS to Azure Service Equivalents: Cloud Service Comparison Matrix

This side-by-side AWS to Azure service mapping compares Amazon Web Services and Microsoft Azure services and entities for engineers doing multi-cloud design, cloud migration, and hybrid architecture. It covers compute, storage, databases, networking, identity, security, monitoring, analytics, AI/ML, containers, IoT, DevOps, and more, with the closest Azure equivalent and a short description for each AWS service or entity.

## How to use this reference

Mappings are approximate. The closest Azure equivalent often differs in features, limits, quotas, regional availability, and pricing, so verify details against the official AWS and Azure documentation before making design decisions. Last reviewed: 2026-11.

## Table of Contents

- [Compute](#compute)
- [Containers](#containers)
- [Storage](#storage)
- [Databases](#databases)
- [Networking](#networking)
- [Identity & Access](#identity--access)
- [Security](#security)
- [Monitoring & Logging](#monitoring--logging)
- [Analytics](#analytics)
- [Machine Learning](#machine-learning)
- [DevOps & Management](#devops--management)
- [Developer Tools](#developer-tools)
- [Migration](#migration)
- [IoT](#iot)
- [Blockchain](#blockchain)
- [Media Services](#media-services)
- [Contributing](#contributing)
- [License](#license)

## Compute

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **Compute** | Amazon EC2 | Azure Virtual Machines | Virtual servers for general compute. |
| **Compute** | AWS Lambda | Azure Functions | Serverless computing to run code without provisioning servers. |
| **Compute** | AWS Elastic Beanstalk | Azure App Service | Platform-as-a-Service (PaaS) for web applications and APIs. |
| **Compute** | AWS Auto Scaling | Azure Virtual Machine Scale Sets | Automatic scaling of virtual machines. |
| **Compute** | AWS Batch | Azure Batch | Managed batch processing at scale. |
| **Compute** | Spot Instance | Spot VM | Access to unused compute capacity at lower cost. |
| **Compute** | Elastic IP | Static Public IP Address | Allocates fixed IP addresses for dynamic workloads. |
| **Compute** | Instance Metadata Service | Azure Instance Metadata Service | Provides metadata about VM instances. |

## Containers

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **Containers** | Amazon ECS | Azure Container Apps / AKS | Managed container orchestration service. |
| **Containers** | AWS Fargate | Azure Container Instances (ACI) | Serverless containers. |

## Storage

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **Storage** | Amazon S3 | Azure Blob Storage | Object storage for scalable data management. |
| **Storage** | Amazon EBS | Azure Managed Disks | Persistent block storage for virtual machines. |
| **Storage** | Amazon S3 Glacier | Azure Archive access tier (Blob Storage) | Cold storage for infrequently accessed data. |
| **Storage** | AWS Storage Gateway | Azure File Sync / Azure Data Box Gateway | Hybrid cloud storage (StorSimple 8000 series reached end of support on December 31, 2022; Microsoft recommends Azure File Sync). |
| **Storage** | Amazon FSx | Azure Files | Managed file storage with SMB and NFS protocols. |
| **Storage** | Snowball Edge | Azure Data Box | Physical devices for large-scale data transfer. Closed to new customers on November 7, 2025. |

## Databases

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **Databases** | Amazon RDS | Azure SQL Database / Azure Database for PostgreSQL, MySQL | Managed relational database services (AWS RDS supports several engines). |
| **Databases** | Amazon Aurora | Azure Database for PostgreSQL / MySQL | High-performance relational databases. |
| **Databases** | Amazon DynamoDB | Azure Cosmos DB | Fully managed NoSQL database service. |
| **Databases** | Amazon Redshift | Azure Synapse Analytics | Data warehousing and analytics. |
| **Databases** | Amazon ElastiCache | Azure Managed Redis | Managed in-memory caching services (Azure Cache for Redis Basic, Standard, and Premium tiers retire on September 30, 2028). |

## Networking

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **Networking** | Amazon VPC | Azure Virtual Network (VNet) | Private virtual networks for secure resource communication. |
| **Networking** | Subnet | Subnet | Subdivisions within a VPC/VNet for organizing resources. |
| **Networking** | Internet Gateway | No direct equivalent (public IP gives access) | Connects a VPC to the internet; in Azure, VMs reach the internet by default when assigned a public IP. |
| **Networking** | NAT Gateway | NAT Gateway | Enables outbound internet traffic for private subnets. |
| **Networking** | Elastic Load Balancing | Azure Load Balancer (L4) / Application Gateway (L7) | Automatic distribution of traffic across resources. |
| **Networking** | Amazon Route 53 | Azure DNS / Azure Traffic Manager | DNS management and traffic routing. |
| **Networking** | AWS Direct Connect | Azure ExpressRoute | Private connections between on-premises and cloud environments. |
| **Networking** | VPC Peering | VNet Peering | Direct network connectivity between virtual networks. |
| **Networking** | PrivateLink | Azure Private Link | Secure connectivity to services over private networks. |
| **Networking** | VPN Connection | VPN Gateway | Encrypted connections between on-premises and cloud networks. |
| **Networking** | Route Table | Route Table | Determines how traffic is routed within a network. |
| **Networking** | Security Groups | Network Security Groups (NSGs) | Controls inbound and outbound traffic to resources. |
| **Networking** | AWS Global Accelerator | Azure Front Door / Azure Traffic Manager | Improves application performance using global edge networks. |

## Identity & Access

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **Identity & Access** | IAM Role | Managed Identity | Provides secure access to resources without hardcoding credentials. |
| **Identity & Access** | IAM Policy | Azure RBAC role definitions | Define permissions for Azure resources (role assignments grant them to users and identities). |
| **Identity & Access** | AWS Organizations | Azure Management Groups | Centralized management of multiple accounts or subscriptions. |
| **Identity & Access** | SAML Federation | Microsoft Entra ID federation | Single sign-on using external identity providers. |

## Security

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **Security** | AWS KMS | Azure Key Vault | Managed encryption key services. |
| **Security** | AWS Secrets Manager | Azure Key Vault Secrets | Secure storage for sensitive data like passwords and keys. |
| **Security** | AWS Shield | Azure DDoS Protection | Managed protection against distributed denial-of-service (DDoS) attacks. |
| **Security** | AWS Security Hub | Microsoft Defender for Cloud | Unified security management and threat protection. |

## Monitoring & Logging

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **Monitoring & Logging** | Amazon CloudWatch | Azure Monitor | Cloud monitoring and observability. |
| **Monitoring & Logging** | AWS CloudTrail | Azure Activity Log | Tracking and auditing cloud resource activity. |
| **Monitoring & Logging** | AWS X-Ray | Azure Application Insights | Distributed tracing for applications. |
| **Monitoring & Logging** | AWS CloudWatch Logs | Azure Monitor Logs | Centralized log monitoring and analysis. |

## Analytics

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **Analytics** | Amazon EMR | Azure HDInsight | Managed big data frameworks. HDInsight 4.0 retired on March 31, 2025; Microsoft directs new big-data workloads to Azure Databricks or Microsoft Fabric. |
| **Analytics** | AWS Glue | Azure Data Factory | Managed ETL (Extract, Transform, Load) services. Azure Data Factory remains supported, and Microsoft positions Fabric Data Factory as the next generation for new projects. |
| **Analytics** | AWS Glue Data Catalog | Microsoft Purview | Metadata management and governance for data assets. |
| **Analytics** | Amazon Athena | Azure Synapse Serverless SQL Pools | Querying data stored in object storage. |
| **Analytics** | Amazon Kinesis | Azure Event Hubs | Real-time data streaming. |

## Machine Learning

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **Machine Learning** | Amazon SageMaker | Azure Machine Learning | Managed machine learning service. |
| **Machine Learning** | AWS Rekognition | Azure Vision in Foundry Tools | Pre-trained computer vision models (part of Foundry Tools, formerly Azure AI Services and Cognitive Services). |
| **Machine Learning** | Amazon Bedrock | Microsoft Foundry Models | Managed access to foundation models from multiple providers, including Azure OpenAI models in Microsoft Foundry. |

## DevOps & Management

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **DevOps & Management** | AWS CodePipeline | Azure DevOps Pipelines / GitHub Actions | Continuous integration and delivery (CI/CD) pipelines. |
| **DevOps & Management** | AWS CloudFormation | ARM Templates / Bicep | Infrastructure-as-Code (IaC) for managing cloud resources. |
| **DevOps & Management** | AWS Systems Manager Parameter Store | Azure App Configuration | Centralized storage of configuration parameters (secrets belong in Azure Key Vault). |

## Developer Tools

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **Developer Tools** | AWS Cloud9 | GitHub Codespaces / VS Code for the Web | Cloud-based integrated development environments (IDEs). AWS Cloud9 closed to new customers on July 25, 2024; existing customers can continue to use it. |

## Migration

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **Migration** | AWS Migration Hub | Azure Migrate | Centralized migration planning and execution tools. AWS Migration Hub closed to new customers on November 7, 2025; AWS directs new users to AWS Transform. |
| **Migration** | AWS Transform MGN (formerly AWS Application Migration Service) | Azure Migrate | Lift-and-shift migration of on-premises workloads (AWS SMS was discontinued in 2022). |
| **Migration** | AWS Snowball | Azure Data Box | Data transfer appliances for large-scale migrations. Snowball Edge closed to new customers on November 7, 2025. |

## IoT

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **IoT** | AWS IoT Core | Azure IoT Hub | Managed IoT device communication. |
| **IoT** | AWS Greengrass | Azure IoT Edge | Local IoT processing and analysis. |

## Blockchain

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **Blockchain** | Amazon QLDB | Azure Confidential Ledger | Tamperproof, cryptographically verifiable ledgers. Amazon QLDB reached end of support on July 31, 2025 (Azure Blockchain Service was retired in 2021). |

## Media Services

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **Media Services** | AWS Elemental MediaConvert | Partner encoders (Bitmovin, MediaKind, Ravnur) | Video encoding and streaming; Azure Media Services was retired on June 30, 2024. |

## Contributing

Contributions are welcome. Please read [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on suggesting new mappings, corrections, or improvements.

## License

This work is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

Copyright 2026 Stanislav
