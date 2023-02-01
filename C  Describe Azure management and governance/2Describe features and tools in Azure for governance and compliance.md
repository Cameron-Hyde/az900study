# Introduction #

## Upon completing this module, you’ll be able to:

>Describe the purpose of Azure Blueprints
>Describe the purpose of Azure Policy
>Describe the purpose of resource locks
>Describe the purpose of the Service Trust portal

# Describe the purpose of Azure Blueprints #

* Azure Blueprints is a service for standardizing cloud subscription or environment deployments and configuring repeatable settings and policies that are applied as new subscriptions are created.
* Artifacts: Components in the blueprint definition, can be a policy assignment, Azure Resource Manager templates, resource groups, etc.
* Artifacts can have parameters that can be configured at the time of blueprint definition or blueprint assignment to a scope.
* Azure Blueprints are version-able, allowing you to make updates and keep track of which deployments used which configuration set.
* The relationship between the blueprint definition and the blueprint assignment is preserved, which helps track and audit deployments.

# Describe the purpose of Azure Policy #

* Enables creation, assignment, and management of policies to control and audit resources in Azure
* Defines rules and ensures resource configurations stay compliant with corporate standards
* Policy definitions can be set at different levels and are inherited down the resource hierarchy
* Azure Policy comes with built-in policies for Storage, Networking, Compute, Security Center, and Monitoring
* Can automatically remediate non-compliant resources and configurations
* Integrates with Azure DevOps for CI/CD pipeline policies
* Azure Policy initiatives are a way of grouping related policies together to track compliance state for a larger goal

# Describe the purpose of resource locks #

* Purpose of Resource Locks: To prevent accidental deletion or changes to critical cloud resources in Azure.

* Types of Resource Locks:
>Delete: Prevents users from deleting the resource, but allows read and modify.
>ReadOnly: Prevents users from deleting or updating the resource, allows only read.
* How to manage Resource Locks: Can be managed using Azure portal, PowerShell, Azure CLI, or Azure Resource Manager template.
* Deleting or changing a locked resource: A two-step process where the lock must first be removed before the change can be made. Resource locks apply regardless of RBAC permissions.

# Exercise - Configure a resource lock #

* Azure Resource Locks can be used to prevent unintended deletion or modification of Azure resources.
* Resource locks are applied to a resource group or individual resources like storage accounts, virtual machines, and databases.
* There are two types of locks: Read-only lock and Delete lock.
* Read-only lock prevents the update or deletion of resources in a resource group or individual resource.
* Delete lock prevents deletion of resources in a resource group or individual resource.
* To apply a resource lock, you must have an Azure resource created first, like a storage account.
* The lock can be applied via Azure portal by going to Settings > Locks and then adding a lock.
* To modify or remove a resource lock, navigate to Settings > Locks, select the lock and modify/delete as desired.
Locks do not prevent resource changes made by Azure services.

# Describe the purpose of the Service Trust portal #

* Microsoft Service Trust Portal is a portal that provides access to information, tools, and resources about Microsoft's security, privacy, and compliance practices.
* To access some resources, you need to sign in with a Microsoft cloud services account (Azure Active Directory organization account) and accept the Microsoft non-disclosure agreement for compliance materials.
* You can access the Service Trust Portal at https://servicetrust.microsoft.com/
* The main menu categories are:
* Service Trust Portal (home page)
* My Library (to save/pin documents)
* All Documents (single landing place for documents)
* Service Trust Portal reports and documents are available for at least 12 months or until a new version becomes available.

1. How many parameters does an Azure Blueprint Artifact need to be valid?
>0:  It is possible for artifacts to have no additional parameters. An example is the Deploy threat detection on SQL servers policy, which requires no additional configuration.
2. How can you prevent non-compliant resources from being created, without having to manually evaluate each resource as it’s created?
>Azure policy lets you create policies and initiatives (groups of policies) that prevent non-compliant resource from being created.
