# Azure Security Notes

Notes for Azure Security Presentation

## Azure Security

Specifically content for developers including websites, web services, web apps, and database/data warehouse.

Topics include:

## Azure App Services Security

### 1. Azure App Services Web Apps or Web Apps (PAAS) -
  * Definition -
      * Most common choice for deploying web app/sites, REST API's, and mobile back ends. .NET, .NET Core, Jara, Ruby, Node.js, or Python         can be used.
  * Features -
      * Load balancing and traffic manager provide high availability. Scaling is also a feature. DevOps capabilities are incorporated such         as continuous deployment utilizing Azure DevOps, Git, Docker Hub, and more....
  * Built-In Azure Security -
      * Azure web apps run within their own isolated sandbox environment
      * VM instances and runtime software receive regular updates
      * Secure secrets including connection strings between apps and Azure resources do not cross network boundaries
      * All connections using App Service connectivity are encrypted
      * Connections using remote connections tools ie PowerShell are encrypted
  * Azure additional security
      * HTTPS and Certificates - by default app is created with https access
      * Static IP restrictions - it is possible to restrict access by IP address to app
      * Service to service authentication - Service identity (app managed identity) or On-behalf-of (delegated access)
      * Connectivity to remote resources - S2S VPN Tunnel
