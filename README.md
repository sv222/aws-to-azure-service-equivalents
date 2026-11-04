# AWS to Azure Service Equivalents

The tables map AWS services to their closest Azure equivalents. Each row gives the Azure equivalent and a short note on the AWS service, including partial matches and retirement dates.

## How to use this reference

Mappings are approximate. The closest Azure equivalent often differs in features, limits, quotas, regional availability, and pricing, so verify details against the official AWS and Azure documentation before making design decisions. Last reviewed: 2026-11.

## Table of Contents

- [Compute](#compute)
- [Containers](#containers)
- [Storage](#storage)
- [Databases](#databases)
- [Time Series Database](#time-series-database)
- [Networking](#networking)
- [Integration & Messaging](#integration--messaging)
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
| **Compute** | AWS Elastic Beanstalk | Azure App Service | Deploys and scales web applications without managing the underlying infrastructure. |
| **Compute** | AWS Auto Scaling | Azure Virtual Machine Scale Sets | Automatic scaling of virtual machines. |
| **Compute** | AWS Batch | Azure Batch | Managed batch processing at scale. |
| **Compute** | Spot Instance | Spot VM | Access to unused compute capacity at lower cost. |
| **Compute** | Elastic IP | Static Public IP Address | Allocates fixed IP addresses for dynamic workloads. |
| **Compute** | Instance Metadata Service | Azure Instance Metadata Service | Provides metadata about VM instances. |
| **Compute** | AWS Outposts | Azure Local | Fully managed AWS infrastructure for on-premises workloads; Azure Local (formerly Azure Stack HCI) is hybrid infrastructure enabled by Azure Arc. |

## Containers

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **Containers** | Amazon ECS | Azure Container Apps | Managed container orchestration service. |
| **Containers** | AWS Fargate | Azure Container Instances (ACI) / Azure Container Apps | Serverless compute for containers that run Amazon ECS tasks and Amazon EKS pods. |
| **Containers** | Amazon EKS | Azure Kubernetes Service (AKS) | Managed Kubernetes service. |
| **Containers** | Amazon EKS Auto Mode | AKS Automatic | Kubernetes cluster mode that automates node, compute, storage, and networking management. |
| **Containers** | Amazon ECR | Azure Container Registry | Managed private registry for storing and deploying container images. |
| **Containers** | AWS App Runner | Azure App Service / Azure Container Apps | Fully managed service for containerized web applications and APIs; closed to new customers on April 30, 2026. |

## Storage

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **Storage** | Amazon S3 | Azure Blob Storage | Object storage for scalable data management. |
| **Storage** | Amazon EBS | Azure Managed Disks | Persistent block storage for virtual machines. |
| **Storage** | Amazon S3 Glacier | Azure Archive access tier (Blob Storage) | Cold storage for infrequently accessed data. |
| **Storage** | AWS Storage Gateway | Azure File Sync / Azure Data Box Gateway | Hybrid cloud storage (StorSimple 8000 series reached end of support on December 31, 2022; Microsoft recommends Azure File Sync). |
| **Storage** | Amazon FSx | Azure Files | Managed file storage with SMB and NFS protocols. |
| **Storage** | Snowball Edge | Azure Data Box | Physical devices for large-scale data transfer. Closed to new customers on November 7, 2025. |
| **Storage** | Amazon EFS | Azure Files | Serverless, elastic NFS file storage for Linux clients; Azure Files also supports SMB. |
| **Storage** | Amazon FSx for NetApp ONTAP | Azure NetApp Files | Fully managed file storage built on NetApp ONTAP. |
| **Storage** | AWS Backup | Azure Backup | Centralized, policy-based backup service across AWS services. |
| **Storage** | AWS Elastic Disaster Recovery | Azure Site Recovery | Disaster recovery service that replicates servers to AWS for failover and failback. |

## Databases

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **Databases** | Amazon RDS | Azure SQL Database / Azure Database for PostgreSQL, MySQL | Managed relational database services (AWS RDS supports several engines). |
| **Databases** | Amazon Aurora | Azure Database for PostgreSQL / MySQL | High-performance relational databases. |
| **Databases** | Amazon DynamoDB | Azure Cosmos DB | Fully managed NoSQL database service. |
| **Databases** | Amazon Redshift | Azure Synapse Analytics or Microsoft Fabric Warehouse | Data warehousing and analytics. |
| **Databases** | Amazon ElastiCache | Azure Managed Redis | Managed in-memory caching services (Azure Cache for Redis Basic, Standard, and Premium tiers retire on September 30, 2028; Enterprise and Enterprise Flash tiers retire on March 31, 2027). |
| **Databases** | Amazon DocumentDB | Azure Cosmos DB for MongoDB | Fully managed, MongoDB-compatible document database service; verify API feature support, which differs between the two. |
| **Databases** | Amazon Keyspaces | Azure Cosmos DB for Apache Cassandra | Serverless, managed database with a CQL API compatible with Apache Cassandra; Azure Managed Instance for Apache Cassandra runs open-source Cassandra clusters. |
| **Databases** | Amazon MemoryDB | Azure Managed Redis | Durable, in-memory database compatible with Valkey and Redis OSS; confirm persistence requirements against Azure Managed Redis documentation. |

## Time Series Database

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **Time Series Database** | Amazon Timestream | Azure Data Explorer | Time series database service; Timestream for LiveAnalytics closed to new customers on June 20, 2025, while Timestream for InfluxDB remains available, and Azure Data Explorer is a close analog for time series analytics, not a drop-in replacement. |

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
| **Networking** | Amazon API Gateway | Azure API Management | Managed service to create, publish, maintain, monitor, and secure APIs. |
| **Networking** | Amazon CloudFront | Azure Front Door | Global content delivery network and application delivery service. |
| **Networking** | AWS WAF | Azure Web Application Firewall | Protects web applications from common exploits and bot traffic; Azure WAF runs on Azure Front Door or Application Gateway. |
| **Networking** | AWS Transit Gateway | Azure Virtual WAN | Hub that interconnects virtual networks, on-premises sites, and VPN connections; Virtual WAN uses Microsoft-managed hubs with different routing behavior. |
| **Networking** | AWS Network Firewall | Azure Firewall | Managed, stateful network firewall service that protects virtual network resources. |
| **Networking** | AWS Client VPN | VPN Gateway (point-to-site) | Managed VPN that connects individual client devices to a virtual network. |

## Integration & Messaging

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **Integration & Messaging** | Amazon SQS | Azure Service Bus | Managed message queues that decouple application components. |
| **Integration & Messaging** | Amazon SNS | Azure Service Bus topics | Publish-subscribe messaging that fans out messages to multiple subscribers. |
| **Integration & Messaging** | Amazon EventBridge | Azure Event Grid | Event routing that delivers events from publishers to subscribers and handlers. |
| **Integration & Messaging** | AWS Step Functions | Azure Logic Apps | Workflow orchestration that coordinates steps and services through triggers and actions. |
| **Integration & Messaging** | Amazon MQ | Azure Service Bus | Managed Apache ActiveMQ and RabbitMQ message brokers; Azure Service Bus is a different broker, so migration requires client changes. |
| **Integration & Messaging** | Amazon SES | Azure Communication Services Email | Managed email sending for transactional and bulk email from custom domains. |

## Identity & Access

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **Identity & Access** | IAM Role | Managed Identity | Provides secure access to resources without hardcoding credentials. |
| **Identity & Access** | IAM Policy | Azure RBAC role definitions | Define permissions for Azure resources (role assignments grant them to users and identities). |
| **Identity & Access** | AWS Organizations | Azure Management Groups | Centralized management of multiple accounts or subscriptions. |
| **Identity & Access** | SAML Federation | Microsoft Entra ID federation | Single sign-on using external identity providers. |
| **Identity & Access** | Amazon Cognito | Microsoft Entra External ID | Customer identity and sign-up and sign-in for applications; Azure AD B2C closed to new customers on May 1, 2025. |
| **Identity & Access** | AWS IAM Identity Center | Microsoft Entra ID | Single sign-on for workforce users to cloud and SaaS applications. |
| **Identity & Access** | AWS Directory Service | Microsoft Entra Domain Services | Managed Active Directory domain services, including domain join, Group Policy, LDAP, and Kerberos/NTLM authentication. |
| **Identity & Access** | AWS Control Tower | Azure landing zones | Architecture guidance and deployment accelerators for a governed, multi-subscription environment; Azure landing zones are not a single managed service. |

## Security

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **Security** | AWS KMS | Azure Key Vault | Managed encryption key services. |
| **Security** | AWS Secrets Manager | Azure Key Vault Secrets | Secure storage for sensitive data like passwords and keys. |
| **Security** | AWS Shield | Azure DDoS Protection | Managed protection against distributed denial-of-service (DDoS) attacks. |
| **Security** | AWS Security Hub | Microsoft Defender for Cloud | Unified security management and threat protection. |
| **Security** | Amazon GuardDuty | Microsoft Defender for Cloud | Threat detection for cloud accounts and workloads; Defender for Cloud also provides security posture management. |
| **Security** | Amazon Inspector | Microsoft Defender Vulnerability Management | Continuous vulnerability discovery, assessment, and risk-based prioritization. |
| **Security** | Amazon Macie | Microsoft Purview | Discovers and classifies sensitive data; Purview covers a wider data estate than Macie's Amazon S3 scope. |
| **Security** | AWS Certificate Manager | Azure Key Vault certificates | Stores and manages X.509 certificates with lifetime alerts; public TLS certificates come from partner certificate authorities. |
| **Security** | AWS CloudHSM | Azure Cloud HSM | Single-tenant, FIPS 140-3 Level 3 validated hardware security modules that customers administer. |
| **Security** | Amazon Security Lake | Microsoft Sentinel data lake | Security data lake that centralizes security telemetry in an open format for analytics. |

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
| **Analytics** | Amazon MSK | Azure Event Hubs for Apache Kafka | Managed Apache Kafka-compatible streaming through an Event Hubs Kafka endpoint, without running Kafka brokers. |
| **Analytics** | Amazon Data Firehose | Azure Event Hubs Capture | Continuously delivers streaming data to Blob Storage or Data Lake Storage; a feature of Azure Event Hubs. |
| **Analytics** | Amazon Managed Service for Apache Flink | Azure Stream Analytics | Real-time stream processing with a SQL-based query language; Flink applications written against the DataStream API need rewriting. |

## Machine Learning

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **Machine Learning** | Amazon SageMaker | Azure Machine Learning | Managed machine learning service. |
| **Machine Learning** | AWS Rekognition | Azure Vision in Foundry Tools | Pre-trained computer vision models (part of Foundry Tools, formerly Azure AI Services and Cognitive Services). |
| **Machine Learning** | Amazon Bedrock | Microsoft Foundry Models | Managed access to foundation models from multiple providers, including Azure OpenAI models in Microsoft Foundry. |
| **Machine Learning** | Amazon Textract | Azure Document Intelligence in Foundry Tools | Extracts text and structured data from scanned documents and images. |
| **Machine Learning** | Amazon Comprehend | Azure Language in Foundry Tools | Natural language processing for entity, key phrase, sentiment, and language detection. |
| **Machine Learning** | Amazon Translate | Azure Translator in Foundry Tools | Neural machine translation service for text and documents. |
| **Machine Learning** | Amazon Transcribe | Azure Speech in Foundry Tools | Automatic speech recognition service that converts audio to text. |
| **Machine Learning** | Amazon Polly | Azure Speech in Foundry Tools | Text-to-speech service that synthesizes speech from text. |
| **Machine Learning** | Amazon Kendra | Azure AI Search | Intelligent enterprise search service. |

## DevOps & Management

| **Category** | **AWS Service/Entity** | **Azure Equivalent** | **Description** |
|---|---|---|---|
| **DevOps & Management** | AWS CodePipeline | Azure DevOps Pipelines / GitHub Actions | Continuous integration and delivery (CI/CD) pipelines. |
| **DevOps & Management** | AWS CloudFormation | ARM Templates / Bicep | Infrastructure-as-Code (IaC) for managing cloud resources. |
| **DevOps & Management** | AWS Systems Manager Parameter Store | Azure App Configuration | Centralized storage of configuration parameters (secrets belong in Azure Key Vault). |
| **DevOps & Management** | AWS CodeBuild | Azure Pipelines | Managed build service that compiles code, runs tests, and produces artifacts. |
| **DevOps & Management** | AWS CodeCommit | Azure Repos | Hosted Git repositories with pull requests and code review. |
| **DevOps & Management** | AWS CodeArtifact | Azure Artifacts | Managed package feeds that store and share packages for npm, NuGet, Maven, Python, and other package types. |
| **DevOps & Management** | AWS Config | Azure Policy | Evaluates resource configurations against rules to audit compliance and enforce organizational standards. |
| **DevOps & Management** | AWS Cost Explorer | Microsoft Cost Management | Cost analysis, budgets, and alerts for reviewing and optimizing cloud spending. |
| **DevOps & Management** | AWS Trusted Advisor | Azure Advisor | Personalized recommendations for cost, performance, security, reliability, and operational excellence. |
| **DevOps & Management** | AWS Health Dashboard | Azure Service Health | Notifications about service issues and planned maintenance that affect your resources. |
| **DevOps & Management** | AWS Service Catalog | Azure Managed Applications | Internal catalog of approved solutions that users deploy; Azure Managed Applications packages solutions for an internal service catalog. |

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
| **IoT** | AWS IoT Device Defender | Microsoft Defender for IoT | Security audits and threat detection for IoT and OT devices and networks. |

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

Copyright 2024-2026 Stanislav
