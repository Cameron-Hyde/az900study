# Introduction #

## Upon completing this module, you’ll be able to:

>Describe Azure portal
>Describe Azure Cloud Shell, including Azure CLI and Azure PowerShell
>Describe the purpose of Azure Arc
>Describe Azure Resource Manager (ARM) and Azure ARM templates

# Describe tools for interacting with Azure #

* Azure portal: a web-based, unified console that provides a graphical user interface for managing Azure subscriptions and resources. It is resilient, continuously available, and requires no downtime for maintenance.
* Azure Cloud Shell: a browser-based shell tool that supports both Azure PowerShell and Azure Command Line Interface (CLI), authenticated to your Azure credentials, with no local installation or configuration required.
* Azure PowerShell: a shell for developers, DevOps, and IT professionals to run command-lets (cmdlets) for performing management tasks in Azure using the Azure REST API. It is available via Azure Cloud Shell and can be installed and configured on Windows, Linux, and Mac platforms.
* Azure CLI: functionally equivalent to Azure PowerShell, using Bash commands instead of PowerShell commands, installable on Windows, Linux, and Mac platforms, and accessible through Azure Cloud Shell.

# Describe the purpose of Azure Arc #

* Azure Arc helps to manage hybrid and multi-cloud environments.
* Azure Arc enables extension of Azure compliance and monitoring to hybrid and multi-cloud configurations.
* Azure Arc provides centralized, unified way of managing resources and services, regardless of where they are hosted.
* Azure Arc supports management of on-premises servers, Kubernetes clusters, Azure data services, SQL Server and virtual machines.

# Describe Azure Resource Manager and Azure (ARM) templates #


* Deployment and management service for Azure resources
>Management layer that enables creation, update, and deletion of resources
>Involved in all actions taken with Azure resources
>Consistent results and capabilities in all Azure tools due to ARM handling requests through the same API

* Benefits of ARM:
>Manage infrastructure through declarative templates rather than scripts
>Deploy, manage, and monitor all solution resources as a group
>Re-deploy solution throughout development life-cycle with confidence in consistent state
>Define resource dependencies for correct order of deployment
>Apply access control through RBAC integration
>Organize resources with tags for billing purposes

* ARM Templates:
>Example of infrastructure as code
>Declarative JSON format for describing desired resources
>Code is verified before deployment for correct creation and connection of resources
>Template orchestrates creation of resources in parallel

* Benefits of ARM Templates:
>Declarative syntax
>Repeatable results
>Resource orchestration
>Modular files
>Extensibility through deployment scripts (PowerShell or Bash)

# Knowledge Check #

1. What service helps you manage your Azure, on-premises, and multi-cloud environments?
>Azure Arc, working with Azure Resource Manager, lets you extend your Azure compliance and monitoring to your hybrid and multi-cloud configurations.
2. What two components could you use to implement a “infrastructure as code” deployment?
>Azure Blueprints applies policies in an automated fashion and ARM Templates allow you to deploy your resource as code. Using the two together helps ensure that you’re deploying consistent, compliant resources.