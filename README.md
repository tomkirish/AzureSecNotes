# Azure Security Notes

Notes for Azure Security Presentation

## Azure Security

Specifically content for developers including websites, web services, web apps, and database/data warehouse.

Topics include:

## Azure App Services Security

### 1. Azure App Services Web Apps or Web Apps (PAAS) -

* Definition -

  * Most common choice for deploying web app/sites, REST API's, and mobile back ends. .NET, .NET Core, Jara, Ruby, Node.js, or Python can be used.

* Features -
  
  * Load balancing and traffic manager provide high availability. Scaling is also a feature. DevOps capabilities are incorporated such as continuous deployment utilizing Azure DevOps, Git, Docker Hub, and more....

* Built-In Azure Security -
  
  * Azure web apps run within their own isolated sandbox environment
  * VM instances and runtime software receive regular updates
  * Secure secrets including connection strings between apps and Azure resources do not cross network boundaries
  * All connections using App Service connectivity are encrypted
  * Connections using remote connections tools ie PowerShell are encrypted

* Azure additional security -

  * HTTPS and Certificates - by default app is created with https access
  * Static IP restrictions - it is possible to restrict access by IP address to app
  * Service to service authentication - Service identity (app managed identity) or On-behalf-of (delegated access)
  * Connectivity to remote resources - S2S VPN Tunnel

### 2. Azure App Service Environment (ASE) -

* Definition -

  * Essentially Azure web apps that can be implemented in client's Azure environment.

* Features -

  * The same apps can be deployed such as Windows and Linux web apps, Docker containers, Mobile apps, and Functions. Usually meant for very high scaling, isolation and secure network access, and/or high memory utilization.

* Azure Security Options -

  * Dedicated environment
  * Azure Firewall with supported VNets
  * Service Endpoints - SQL, storage, key vault
  * SSL/HTTPS

### 3. Azure VM's (IAAS) -

* Definition -

  * An Azure VM allows for just about any workload running on almost any operating system.

* Features -

  * Using VMs allows for more customization and isolation in case you are outside of what web apps supports. Azure VMs work with the following services Windows, Linux, SQL, Oracle, IBM, SAP and BizTalk Services.

* Security Options -

  * AntiMalware
  * Hardware security module (HSM) - Key Vault
  * Encrypt data using data encryption at rest (Gen 2 Storage or Bitlocker) and in transit (SSL)
  * Network Security Groups
  * Firewalls
  * Compliance - FISMA, HIPAA, PCI DSS Level 1

### 4. Service Fabric (MicroServices) -

* Definition -

  * A distributed systems (Containers) platform to allow for easy packaging and deploying MicroServices. Service Fabric orchestrates services across a cluster of machines. Containers are the current standard for deploying applications over virtual machines.

* Security -

  * Cluster security
  * Node to node security
  * Client to node security

## General Azure Security Options -

* Azure Active Directory - Primary authentication/authorization mechanism for Azure resources.
* Role Based Access Control - Create roles to allow granular access to Azure resources.
* Key Vault - Key management for secrets and identities.
* Managed Identities - Automatically managed identity in Azure AD.
* Virtual Network Service Endpoints - Allows direct access to resources versus traffic going across Azure public network (internet).

## Azure Database Security

### 1. Azure SQL (PAAS) -

* Definition -

  * SQL database service is a managed database service using the latest version of the SQL engine.

* Features -

  * SQL as a service allows for scaling, advanced analytic features and is completely managed.

* Security -

  * Data encryption in motion using Transport Layer Security
  * Data encryption at rest
  * Data encryption in use
  * Firewall Rules - restrict access to servers, offices, remote admins, etc...
  * Azure Active Directory authentication
  * Role-based memberships and permissions to manage data
  * Row level security
  * Dynamic Data Masking

### 2. SQL on Azure VMs (IAAS) -

* Definition -

  * Utilizing Azure VM's to perform SQL workload

* Features -
  * Use when customization, security, additional features are needed and fall outside of the SQL as a service support model

* Security -
  * Azure Active Directory
  * SQL Logins
  * Create firewall and NSG access
  * Must maintain all security

### 3. Managed Instances (PAAS) -

* Definition -

  * New deployment model of Azure SQL providing compatibility with on-premise SQL Enterprise.

* Features -

  * Designed to allow for easier lift and shift of on premise SQL databases while maintaining PAAS functionality.

* Security -
  * Same security features as Azure SQL

### 4. SQL Data Warehouse (PAAS) -

* Definition -

  * Enterprise level cloud based SQL Data Warehouse that leverages Massively Parallel Processing for complex queries.

* Features -

  * Separates compute from storage which enables compute to scale independently of the data in the system

* Security

  * Firewall rules
  * Azure Active Directory
  * Connections are encrypted
  * Role memberships and permissions
  * Encryption

### 5. CosmosDB (PAAS) -

* Definition -

  * Provide native support for No SQL and OSS API's including Mongo DB, Cassandra, SQL, and more.

* Features -
  * Guaranteed low latency with push button elastic scalability and global distribution.

* Security -

  * Encryption at rest
  * Master keys and Resource tokens for data access
  * Firewall rules
  * Endpoint support
  * KeyVault support

### 6. Azure for MySQL (PAAS) -

* Definition -

  * Relational database service based on MySQL server.

* Security -

  * Service is not exposed to the internet
  * SSL support for application connections
  * Encryption at rest

## Glossary

### Azure Security General

* <https://www.microsoft.com/en-us/azureessentials>
* <https://docs.microsoft.com/en-us/azure/security/azure-security>
* <https://docs.microsoft.com/en-us/azure/security/security-best-practices-and-patterns>
* <https://www.microsoft.com/handsonlabs/selfpacedlabs#keywords=security&page=1&sort=Newest>
* <https://www.edx.org/course/microsoft-azure-security-services-0>
* <https://github.com/MicrosoftDocs/azure-docs/blob/master/articles/security/security-best-practices-and-patterns.md>

### Azure Security Center

* <https://docs.microsoft.com/en-us/azure/security-center/security-center-planning-and-operations-guide>
* <https://docs.microsoft.com/en-us/azure/security-center/security-center-faq>
* <https://www.microsoft.com/en-us/azureessentials/Pivot/AzureEssentials/SecurityCenter/Learn>
* <https://docs.microsoft.com/en-us/azure/security-center/>
* <https://mva.microsoft.com/en-US/training-courses/introduction-to-azure-security-center-16614?l=BUOzJ6znC_9504300474>
* <https://mva.microsoft.com/en-US/training-courses/hybrid-cloud-workload-protection-with-azure-security-center-18173?l=Ld0LK42jE_006218965>
* <https://channel9.msdn.com/Blogs/Azure-Security-Videos>

### Encryption

https://docs.microsoft.com/en-us/azure/storage/common/storage-service-encryption
https://docs.microsoft.com/en-us/azure/security/azure-security-encryption-atrest
https://docs.microsoft.com/en-us/azure/security/azure-security-data-encryption-best-practices
https://docs.microsoft.com/en-us/azure/security/security-azure-encryption-overview
https://azure.microsoft.com/en-us/updates/azure-backup-sse-encryption-at-rest/
https://docs.microsoft.com/en-us/azure/storage/common/storage-service-encryption-customer-managed-keys
https://azure.microsoft.com/en-us/blog/announcing-default-encryption-for-azure-blobs-files-table-and-queue-storage/

### Storage Security

https://docs.microsoft.com/en-us/azure/storage/common/storage-security-guide
https://docs.microsoft.com/en-us/azure/security/azure-security-disk-encryption-overview

### Network Security

https://docs.microsoft.com/en-us/azure/security/azure-security-network-security-best-practices
https://docs.microsoft.com/en-us/azure/application-gateway/application-gateway-web-application-firewall-overview
https://docs.microsoft.com/en-us/azure/virtual-network/security-overview
https://docs.microsoft.com/en-us/azure/virtual-network/ddos-protection-overview
https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-vnet-plan-design-arm

### Azure Advisor

Example - 


https://docs.microsoft.com/en-us/azure/advisor/advisor-overview

### Identity Security
https://docs.microsoft.com/en-us/azure/security/azure-security-identity-management-best-practices

### RBAC
https://docs.microsoft.com/en-us/azure/role-based-access-control/overview

### Azure Admin Portal

https://docs.microsoft.com/en-us/azure/role-based-access-control/role-assignments-portal
Development Security

### Azure Key Vault

https://docs.microsoft.com/en-us/azure/key-vault/key-vault-whatis
### Virtual Network Service EndPoints

https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-service-endpoints-overview
https://docs.microsoft.com/en-us/azure/virtual-network/tutorial-restrict-network-access-to-resources

### Database Security

#### SQL

https://docs.microsoft.com/en-us/sql/relational-databases/security/encryption/transparent-data-encryption-azure-sql?view=azuresqldb-current
https://docs.microsoft.com/en-us/azure/sql-database/sql-database-security-overview
https://docs.microsoft.com/en-us/azure/sql-database/sql-database-always-encrypted-azure-key-vault

#### Cosmos DB

https://docs.microsoft.com/en-us/azure/cosmos-db/database-encryption-at-rest
https://docs.microsoft.com/en-us/azure/cosmos-db/database-security

### Quick Deployment

https://github.com/Azure/azure-quickstart-templates

### Azure Security Blog

https://azure.microsoft.com/en-us/blog/topics/security/

### Azure Marketplace - Security Solutions
https://azuremarketplace.microsoft.com/en-us/marketplace/apps/category/security-identity

#### Other 3rd Party solutions

https://cloudcheckr.com/
https://www.cloudhealthtech.com/

### Security Information & Event Management (SIEM)

https://www.logrhythm.com/
https://www.splunk.com/

### Microsoft Security General

https://www.microsoft.com/en-us/trustcenter/default.aspx
