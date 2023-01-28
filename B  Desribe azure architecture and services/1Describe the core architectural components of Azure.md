# Introduction #

## Upon completing this module, you’ll be able to:
>Describe Azure regions, region pairs, and sovereign regions.
>Describe Availability Zones.
>Describe Azure datacenters.
>Describe Azure resources and Resource Groups.
>Describe subscriptions.
>Describe management groups.
>Describe the hierarchy of resource groups, subscriptions, and management groups.

# What is Microsoft Azure #

* Azure is a continually expanding set of cloud services that help you meet current and future business challenges
* Azure gives you the freedom to build, manage, and deploy applications on a massive global network using your favorite tools and frameworks
* Azure provides continuous innovation from Microsoft to support your development today and your product visions for tomorrow
* Azure provides choices with a commitment to open source, and support for all languages and frameworks, you can build how you want and deploy where you want
* Azure provides seamless operation of hybrid environments, on-premises, in the cloud, and at the edge
* Azure provides security from the ground up, backed by a team of experts, and proactive compliance trusted by enterprises, governments, and startups
* Azure provides more than 100 services that enable you to do everything from running your existing applications on virtual machines to exploring new software paradigms, such as intelligent bots and mixed reality
* Azure services enable solutions that aren't feasible without the power of the cloud.

# Get Started With Azure Accounts #

* To create and use Azure services, you need an Azure subscription.
* A temporary subscription can be created for you in an environment called the Learn sandbox when completing Learn modules.
* When working with your own applications, you need to create an Azure account and a subscription. Additional subscriptions can be created for different departments or purposes.
* Azure provides a free account option for new users to start exploring at no cost.
* Azure access can be purchased directly from Microsoft or through a Microsoft partner.
* The Azure free account includes free access to popular Azure products for 12 months, a credit to use for the first 30 days, and access to more than 25 products that are always free.
* The Azure free student account offer includes free access to certain Azure services for 12 months, a credit to use in the first 12 months, and free access to certain software developer tools.
* The Microsoft Learn sandbox creates a temporary subscription for you to use during Learn modules and automatically cleans up resources after completion.

# Exercise - Explore the Learn sandbox #

* The Learn sandbox is a free resource provided by Microsoft for educational purposes and can only be used to complete training on Microsoft Learn.
* You can interact with the Learn sandbox in three different ways: **PowerShell CLI**, **BASH CLI**, and **Azure CLI interactive mode**.
* To activate the Learn sandbox, use the **Activate sandbox** button and review and accept the permissions.
* In PowerShell CLI mode, use the command `Get-date` to get the current date and time, and `az version` to check the version of the CLI you're using.
* In BASH CLI mode, use the command `bash` to switch to BASH CLI and `date` to get the current date and time. You can use `az upgrade` to update the CLI.
* In Azure CLI interactive mode, use the command `az interactive` to enter interactive mode, which provides autocompletion, command descriptions, and examples. You can use `version` and `upgrade` commands without "az" in front.
* You can also use the Azure portal, which can be accessed through the link provided in the exercise.

# Describe Azure Physical Infrastructure #

* Azure physical infrastructure starts with datacenters, which are grouped into regions or availability zones to provide resiliency and reliability for business-critical workloads.
* A region is a geographical area that contains at least one, but potentially multiple datacenters that are nearby and networked together with a low-latency network.
* Availability zones are physically separate datacenters within an Azure region, each with independent power, cooling, and networking. If one zone goes down, the other continues working.
```
To ensure resiliency, a minimum of three separate availability zones are present in all availability zone-enabled regions
```
* Availability zones are used to run mission-critical applications and build high-availability into application architecture by co-locating resources within an availability zone and replicating in other availability zones.
* Azure services that support availability zones fall into three categories: **zonal services**, **zone-redundant services**, and **non-regional services**.
* To provide even further resilience, Azure has region pairs, which are paired with another region within the same geography at least 300 miles away.
* Region pairs allow for the replication of resources across a geography, reducing the likelihood of interruptions due to events such as natural disasters, civil unrest, power outages, or physical network outages that affect an entire region.
```
Not all Azure services automatically replicate data or automatically fall back from a failed region to cross-replicate to another enabled region, and recovery and replication must be configured by the customer in these scenarios.
```
```
Some regions, such as West India and Brazil South, are paired in only one direction, meaning that the primary region does not provide backup for its secondary region. This means that the secondary region does not rely on the primary region.
Additionally, Brazil South is unique in that it is paired with a region outside of its geography, with its secondary region being South Central US.
```
* Additional advantages of region pairs include prioritization of restoration of one region out of every pair, rolling out planned Azure updates to paired regions one at a time, and data continuing to reside within the same geography as its pair for tax and law-enforcement jurisdiction purposes.

* Azure also has sovereign regions which are isolated from the main instance of Azure and may be required for compliance or legal purposes.
>Examples of Azure sovereign regions include:
>>US DoD Central, US Gov Virginia, US Gov Iowa and more: These regions are physical and logical network-isolated instances of Azure for U.S. government agencies and partners. These datacenters are operated by screened U.S. personnel and include additional compliance certifications.
>>China East, China North, and more: These regions are available through a unique partnership between Microsoft and 21Vianet, whereby Microsoft doesn't directly maintain the datacenters.

# Describe Azure management infrastructure #

* Azure management infrastructure includes resources and resource groups, subscriptions, and accounts
* Resources are the basic building blocks of Azure, anything you create, provision, deploy, etc. is a resource. Virtual Machines (VMs), virtual networks, databases, cognitive services, etc. are all considered resources within Azure.
* Resource groups are groupings of resources, when you create a resource, you’re required to place it into a resource group.
* When you apply an action to a resource group, that action will apply to all the resources within the resource group.
* Subscriptions are a unit of management, billing, and scale, They allow you to logically organize your resource groups and facilitate billing.
* Using Azure requires an Azure subscription. A subscription provides you with authenticated and authorized access to Azure products and services.
* An Azure subscription links to an Azure account, which is an identity in Azure Active Directory (Azure AD) or in a directory that Azure AD trusts.
* Azure subscriptions allow you to define boundaries around Azure products, services, and resources. There are two types of subscription boundaries:
* Billing boundary: This subscription type determines how an Azure account is billed for using Azure.
* Access control boundary: Azure applies access-management policies at the subscription level
* Azure management groups provide a level of scope above subscriptions. You organize subscriptions into containers called management groups and apply governance conditions to the management groups.
* Management groups give you enterprise-grade management at a large scale, no matter what type of subscriptions you might have. Management groups can be nested.

```
It's also worth noting that a single directory can support up to 10,000 management groups, and a management group tree can support up to six levels of depth. Each management group and subscription can only have one parent.
```
# Exercise - Create an Azure resource #

* The module involves creating a virtual machine using the Azure portal
* The virtual machine is created within a resource group, which automatically includes associated resources such as a storage account and virtual network
* The following Azure CLI command can be used to create a virtual machine:
* az vm create `--name` "your-vm-name" `--resource-group` "your-resource-group-name" `--image` "image-name"
* The following Azure CLI command can be used to delete the virtual machine:
* az vm delete `--name` "your-vm-name" `--resource-group` "your-resource-group-name"
* It's important to note that when working in a personal subscription, resources that are no longer needed should be identified and potentially deleted to avoid incurring unnecessary costs.

# Knowledge Check #

1. How many resource groups can a resource be in at the same time?
> once, A resource can only be in one group at a time.
2. What happens to the resources within a resource group when an action or setting at the Resource Group level is applied?
> The setting is applied to current and future resources.
Resources inherit permissions from their resource group.
3. What Azure feature replicates resources across regions that are at least 300 miles away from each other?
> Region pairs
Most Azure regions are paired with another region within the same geography (such as US, Europe, or Asia) at least 300 miles away.