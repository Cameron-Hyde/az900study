# Introduction #

## Upon completing this module, you’ll be able to:

>Describe the purpose of Azure Advisor
>Describe Azure Service Health
>Describe Azure Monitor, including Azure Log Analytics, Azure Monitor Alerts, and Application Insights

# Describe the purpose of Azure Advisor #

* Azure Advisor is a service that provides recommendations to help improve the reliability, security, performance, operational excellence and reduce costs of your Azure resources.
* Azure Advisor provides personalized recommendations for all your Azure subscriptions via the Azure portal and API.
* The recommendations are divided into five categories: Reliability, Security, Performance, Operational Excellence and Cost.
* Azure Advisor dashboard provides a visualization of all the recommendations and can be filtered by specific subscriptions, resource groups, or services.
* Recommendations provided by Azure Advisor include suggested actions that can be taken right away, postponed, or dismissed.

# Describe Azure Service Health #

* Azure Service Health is a tool to help you keep track of Azure resources and overall status of Azure.
* It combines three different Azure services: Azure Status, Service Health, and Resource Health.
* Azure Status provides a broad picture of the status of Azure globally and informs you of service outages in Azure.
* Service Health provides a narrower view of Azure services and regions, focusing on the Azure services and regions you're using. You can set up Service Health alerts to notify you of service issues, planned maintenance, and other health advisories.
* Resource Health provides a tailored view of your actual Azure resources, and informs you of the health of individual cloud resources such as virtual machines. You can configure alerts using Azure Monitor.
* Azure Service Health provides a complete view of your Azure environment, from the global status of Azure services and regions to specific resources.
* Historical alerts are stored and accessible for later review.
* Azure Service Health provides links to support in the event that a workload you're running is impacted by an event.

# Describe Azure Monitor #

* Azure Monitor:
>A platform for collecting data on your resources, analyzing data, visualizing information and acting on results
>Can monitor Azure resources, on-premises resources, and multi-cloud resources
>Flow of information: sources of logging and metric data are collected and stored in central repositories. Data used in several ways (real-time and historical performance, reports, custom views, alerts, etc.)

* Azure Log Analytics:
>Tool in the Azure portal to write and run log queries on the data gathered by Azure Monitor
>Supports simple and complex queries and data analysis
>Result of queries can be used with other Azure Monitor features like log query alerts and workbooks

* Azure Monitor Alerts:
>Automated way to stay informed when Azure Monitor detects a threshold being crossed
>Set up to monitor logs or metrics and notify or take corrective action
>Use action groups to configure who to notify and what action to take

* Application Insights:
>Azure Monitor feature to monitor web applications
>Monitors applications running in Azure, on-premises or other cloud environment
>Two ways to configure: installing an SDK or using the Application Insights agent
>Monitors a broad array of information (request rates, response times, dependency rates, user and session counts, performance counters, etc.)
>Configured to send synthetic requests to monitor the application status even during periods of low activity.

# Knowledge Check #

1. Which is not one of the recommendation categories for Azure Advisor?
>Capacity: The five recommendation categories for Azure Advisor are: Reliability, Security, Performance, Operational Excellence, and Cost.
2. You receive an email notification that virtual machines (VMs) in an Azure region where you have VMs deployed is experiencing an outage. Which component of Azure Service Health will let you know if your application is impacted?
>Resource Health: is a tailored view of your actual Azure resources. It provides information about the health of your individual cloud resources