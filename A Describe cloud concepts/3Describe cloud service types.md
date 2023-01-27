# Introduction #

* This module provides an introduction to different types of cloud services, including Infrastructure as a Service (IaaS), Platform as a Service (PaaS), and Software as a Service (SaaS).
* Each type of cloud service provides different levels of flexibility in managing and configuring resources.
* The shared responsibility model applies to each cloud service type, meaning that the responsibilities of maintaining security and compliance are shared between the cloud service provider and the user.
* The module will also cover appropriate use cases for each cloud service type, such as when to use IaaS, PaaS or SaaS.

# Describe Infrastructure as a Service #

* Infrastructure as a Service (IaaS) is a cloud service category that provides the maximum amount of control for cloud resources.
* In an IaaS model, the cloud provider is responsible for maintaining the hardware, network connectivity, and physical security, while the user is responsible for the operating system, configuration, and maintenance, network configuration, database and storage configuration, etc.
* The shared responsibility model applies to IaaS, with the cloud provider responsible for maintaining the physical infrastructure and access to the internet, while the user is responsible for installation and configuration, patching and updates, and security.
* Common scenarios where IaaS might make sense include: lift-and-shift migration, testing and development, where users need rapid replication of established configurations.

# Describe Platform as a Service #

* Platform as a Service (PaaS) is a type of cloud service that provides a platform for building and deploying applications, including the operating systems, middleware, development tools, and business intelligence services.
* In PaaS environment, the cloud provider is responsible for maintaining the physical infrastructure, physical security, and connection to the internet, as well as the operating systems, middleware, development tools, and business intelligence services.
* PaaS is well suited for providing a complete development environment without the headache of maintaining all the development infrastructure.
* The shared responsibility model applies to PaaS, with the cloud provider being responsible for maintaining the physical infrastructure and its access to the internet, operating systems, databases, and development tools, and the customer is responsible for networking settings and connectivity within the cloud environment, network and application security, and directory infrastructure.
* Common use cases for PaaS include: Development framework, Analytics or business intelligence.

# Describe Software as a Service #

* Software as a Service (SaaS) is the most complete cloud service model, where users rent or use a fully developed application.
* In SaaS, the cloud provider is responsible for physical security of datacenters, power, network connectivity, and application development and patching.
* Users are responsible for the data they put into the system, the devices that connect to the system, and the users that have access.
* SaaS requires the least amount of technical knowledge or expertise to use.
Common examples of SaaS include email, financial software, messaging applications, and connectivity software.
* SaaS is suitable for scenarios such as email and messaging, business productivity applications, and finance and expense tracking.

# Knowledge check #
>1. Which cloud service type is most suited to a lift and shift migration from an on-premises datacenter to a cloud deployment?
    >>With an IaaS service type, you can approximate your on-premises environment, making a lift-and-shift transition to the cloud relatively straightforward.
>2. What type of cloud service type would a Finance and Expense tracking solution typically be in?
    >>SaaS provides access to software solutions, such as finance and expense tracking, email, or ticketing systems.