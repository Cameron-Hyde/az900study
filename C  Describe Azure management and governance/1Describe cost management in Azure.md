# Introduction #

## Upon completing this module, you’ll be able to:
>Describe factors that can affect costs in Azure.
>Compare the Pricing calculator and Total Cost of Ownership (TCO) calculator.
>Describe Azure Cost Management Tool.
>Describe the purpose of tags.

# Describe factors that can affect costs in Azure #
* Resource type: cost of Azure resources depends on the type of resources, the settings for the resource, and the Azure region
* Consumption: pay-as-you-go or reserved capacity model with discounts for committing to use a set amount of resources in advance.
* Maintenance: keeping an eye on your resources to avoid paying for unneeded resources.
* Geography: cost of deploying resources in different regions varies based on local factors such as taxes, power costs, etc.
* Network traffic: billing zones determine the cost of some Azure services, with some inbound data transfers being free and data transfer pricing based on zones for outbound transfers.
* Subscription type: different subscriptions can include usage allowances that affect costs.
* Azure Marketplace: third-party solutions and services can be purchased and their costs added to the overall Azure bill.

# Compare the Pricing and Total Cost of Ownership calculators #

# Pricing Calculator:
>Provides an estimate of the cost of provisioning resources in Azure
>Used to estimate the cost of compute, storage, and network costs
>Used for information purposes only, no resources are provisioned, no charges incurred
>Prices are only an estimate
#Total Cost of Ownership (TCO) Calculator:
>Compares the costs of running an on-premises infrastructure vs Azure Cloud infrastructure
>Enter current infrastructure configuration, including servers, databases, storage, and network traffic
>Includes assumptions like power and IT labor costs
>Presents an estimation of the cost difference between current environment and an Azure environment with the same requirements.

# Exercise - Estimate workload costs by using the Pricing calculator #

* Introduction to the Azure Pricing calculator: an online tool used to estimate the cost of running a workload in Azure
* Before using the calculator, define the Azure services needed for the workload
* The calculator has multiple tabs: Products, Example Scenarios, Saved Estimates, FAQs
* To estimate a solution, add each required Azure service to the calculator and configure it to match the workload requirements
* Configure each service: Virtual Machines, Azure SQL Database, Application Gateway
* Review, share, and save the estimate by selecting Export, Save, Save as, or Share
* The estimated cost is only an approximation and the calculator is for information purposes only, prices are subject to change.

# Exercise - Compare workload costs using the TCO calculator #

* Use the Total Cost of Ownership (TCO) Calculator to compare the cost of running a workload in your datacenter versus on Azure.
* Investigate cost savings of moving from on-premises to the cloud over the next three years.
* TCO Calculator helps with considering hidden costs involved with operating on-premises and in the cloud.
* Run two sets of 50 VMs, first bank with Windows Server under Hyper-V and second bank with Linux under VMware.
* Storage area network with 60 TB disk storage and estimated 15 TB outbound network bandwidth each month.
* TCO Calculator involves three steps: Define your workloads, Adjust assumptions, and View the report.
* Enter specifications of on-premises infrastructure into TCO Calculator under Define Your Workloads section.
* For each bank of VMs, specify values for Name, Workload, Environment, Operating System, Operating System License, VMs, Virtualization, Core(s), RAM, and Optimize by.
* Specify settings for Storage (Local Disk/SAN, HDD, 60 TB, 120 TB, and 0 TB) and Networking (Outbound Bandwidth = 15 TB).
* Adjust currency and remaining fields at default values in Adjust Assumptions section.
* In View Report, set Timeframe to 3 Years and Region to North Europe and review the summary comparison.
* Download or print the report in PDF format.

# Describe the Azure Cost Management tool #

* A tool to monitor and manage Azure resource costs
* Includes cost analysis to view aggregated costs, spending trends, and accumulated costs over time
* Cost alerts:
* Budget alerts: notifies when spending reaches or exceeds defined budget amount
* Credit alerts: notifies when credit commitments are consumed
* Department spending quota alerts: notifies when department spending reaches a fixed threshold
* Budgets: set a spending limit for Azure and can trigger automation when budget alert is triggered
# Note: #

* Cost analysis provides visual for Azure costs
* Cost alerts provide single location to check all different types of alerts
* Budgets are set based on subscription, resource group, service type, etc.
* Budget alerts appear in cost alerts and can send email notifications

# Describe the purpose of tags #

* Resource tags provide extra information or metadata about resources to help with organization and management.
* Resource tags are useful for:
* Resource management: helps locate and act on resources associated with specific workloads, environments, business units, and owners.
* Cost management and optimization: helps group resources for reporting on costs, allocating cost centers, tracking budgets, and forecasting cost.
*Operations management: helps group resources based on their criticality to the business to formulate SLAs.
* Security: helps classify data based on its security level.
* Governance and regulatory compliance: helps identify resources that align with governance or regulatory requirements.
* Workload optimization and automation: helps visualize resources participating in complex deployments.
* Resource tags can be managed through the Azure CLI, Windows PowerShell, REST API, Azure Resource Manager templates, or the Azure portal.
* Azure Policy can enforce tagging rules and conventions.
* Resource tags consist of a name and a value, and can be assigned one or more times to each Azure resource.
* An example tagging structure:
>AppName
>CostCenter
>Owner
>Environment
>Impact.
* The specific tags required for a resource can vary and need not be enforced for all resources.

# Knowledge Check #

1. What Azure feature can help stay organized and track usage based on metadata associated with resources? 
>Tags allow you to associate metadata with a resource to help keep track of resource management, costs and optimization, security, and so on.
2. What’s the best method to estimate the cost of migrating to the cloud while incurring minimal costs?
>Correct. The Total Cost of Ownership calculator lets you input your current infrastructure and requirements and provides you an estimate for running in the cloud.

