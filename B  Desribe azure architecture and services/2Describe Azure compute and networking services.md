# Introduction #

## Upon completing this module, you’ll be able to:
>Compare and contrast different compute types
>Understand the different options and resources required for virtual machines
>Familiarize with various application hosting options such as Azure Web Apps, containers, and virtual machines
>Understand the purpose and function of Azure virtual networks, virtual subnets, peering, Azure DNS, VPN Gateway, and ExpressRoute
>Define public and private endpoints

# Describe Azure Virtual Machines #

* Virtual machines (VMs) are a powerful tool for creating a more resilient, highly available environment.
* Virtual machine availability sets are another tool to help you build a more resilient, highly available environment.
* Availability sets are designed to ensure that VMs stagger updates and have varied power and network connectivity, preventing you from losing all your VMs with a single network or power failure.
* Availability sets do this by grouping VMs in two ways: update domain and fault domain.
* Update domain: The update domain groups VMs that can be rebooted at the same time. This allows you to apply updates while knowing that only one update domain grouping will be offline at a time. All of the machines in one update domain will be updated. An update group going through the update process is given a 30-minute time to recover before maintenance on the next update domain starts.
* Fault domain: The fault domain groups your VMs by common power source and network switch. By default, an availability set will split your VMs across up to three fault domains. This helps protect against a physical power or networking failure by having VMs in different fault domains (thus being connected to different power and networking resources).
* Best of all, there’s no additional cost for configuring an availability set. You only pay for the VM instances you create.
* Examples of when to use VMs include during testing and development, running applications in the cloud, extending your datacenter to the cloud, disaster recovery, and moving to the cloud with VMs.
* When you provision a VM, you’ll also have the chance to pick the resources that are associated with that VM, including size (purpose, number of processor cores, and amount of RAM), storage disks (hard disk drives, solid state drives, etc.), and networking (virtual network, public IP address, and port configuration).

# Exercise - Create an Azure Virtual Machine #

* Creating a Linux virtual machine using the Azure CLI command `az vm create`
* Configuring Nginx on the virtual machine using the Azure CLI command `az vm extension set`
* Using the Custom Script Extension to run a Bash script on the virtual machine
* The Bash script runs `apt-get update` to download the latest package information from the internet
* The Bash script installs Nginx and sets the home page to display a welcome message with the virtual machine's host name
* Updating the network configuration in future units to access the website hosted on the virtual machine.

# Describe Azure Virtual Desktop #

* Azure Virtual Desktop is a desktop/application virtualization service that runs on the cloud
* allows you to use a cloud-hosted version of Windows from any location, from across devices and OS's.
* Azure Virtual Desktop provides centralized security management for users desktops. With Azure Active Directory "Azure AD" you can enable multifactor authentication to secure user sign-ins.
* Use "RBACs"(Granular role-based access controls) to secure access to data
* Azure AD lets you use windows 10 or 11 enterprise multi-session, it is the only Windows client-based os that enables multiple concurrent users on a single VM. 

# Describe Azure Containers #

* Containers are a virtualization environment that allows running multiple instances of an application on a single host machine, unlike virtual machines which require a separate operating system per virtual machine.
* Containers are lightweight and designed to be created, scaled out, and stopped dynamically.
* Azure Container Instances offer a way to run a container in Azure without managing any virtual machines or additional services.
* Containers are often used in microservice architecture, which allows breaking solutions into smaller, independent pieces, making it easier to maintain, scale, and update each component independently.

# Describe Azure Functions #

* Azure Functions is an event-driven, serverless compute option that eliminates the need to maintain virtual machines or containers.
* Azure Functions are ideal for performing work in response to an event, timer, or message from another Azure service, and when that work can be completed quickly within seconds or less.
* Azure Functions scale automatically based on demand, so they may be a good choice when demand is variable.
* Azure Functions charges only for the CPU time used while the function runs.
* Functions can be either stateless or stateful, the default is stateless, it behaves as if they're restarted every time they respond to an event, stateful functions are called Durable Functions, a context is passed through the function to track prior activity.
* Functions are a key component of serverless computing, but also a general compute platform for running any type of code, with the flexibility to manage scaling, run on virtual networks, and isolate the functions.

# Describe application hosting options #

* Azure offers several options for application hosting, including virtual machines (VMs), containers, and Azure App Service.
* Azure App Service is a platform for building and hosting web apps, background jobs, mobile back-ends, and RESTful APIs without managing infrastructure. It offers automatic scaling and high availability, and supports Windows and Linux.
* Types of apps that can be hosted on App Service include web apps, API apps, WebJobs, and mobile apps.
* Web apps can be built and hosted using ASP.NET, ASP.NET Core, Java, Ruby, Node.js, PHP, or Python, and can be hosted on either Windows or Linux.
* API apps can be built as REST-based web APIs using any language and framework, and can be packaged and published in Azure Marketplace.
* WebJobs are used to run programs or scripts in the same context as a web app, API app, or mobile app and can be scheduled or run by a trigger.
* Mobile apps can use the Mobile Apps feature of App Service to quickly build a back-end for iOS and Android apps, including storing data, authenticating customers, and sending push notifications.

# Describe Azure Virtual Networking #

* Azure virtual networks and virtual subnets enable communication between Azure resources, the internet, and on-premises resources
* Azure virtual networks provide key networking capabilities such as isolation and segmentation, internet communications, communication between Azure resources, and communication with on-premises resources
* Azure virtual networking supports both public and private endpoints for communication between external or internal resources
* Isolation and segmentation in Azure virtual networks can be achieved through the use of private IP address ranges and subnets
* For name resolution, Azure virtual networks can use the built-in name resolution service or an internal or external DNS server
* Internet communications can be enabled through the use of public IP addresses or public load balancers
* Communication between Azure resources can be achieved through virtual networks or service endpoints
* Communication with on-premises resources can be achieved through point-to-site VPN connections, site-to-site VPN connections, or Azure ExpressRoute
* Network traffic can be routed and filtered through the use of route tables, Border Gateway Protocol, network security groups, network virtual appliances, and virtual network peering
* User-defined routes allow for greater control over network traffic flow between subnets and virtual networks.

# Exercise - Configure network access and basic clicmd #

* Use the command `az vm list-ip-addresses` to get the IP address of a VM and store the result as a Bash variable
* Use the command `curl --connect-timeout 5 http://$IPADDRESS` to download the home page of the specified IP address
* The `--connect-timeout` argument allows for a maximum of five seconds for the connection to occur.
* Use the command `az vm create` to create a new VM
* Provide necessary parameters such as resource group, VM name, and image
* To connect to the VM, use the command `az vm open-port` to open a specific port, and use ssh to connect to the IP address of the VM
* To start, stop, or restart a VM, use the commands `az vm start`, `az vm stop`, and `az vm restart` respectively.
* To delete a VM, use the command `az vm delete` and provide the name and resource group of the VM
* To list all VMs in a resource group, use the command `az vm list` and provide the resource group name.
* To get the details of a specific VM, use the command `az vm show` and provide the name and resource group of the VM
* To update the VM's configuration, use the command `az vm update` and provide the name and resource group of the VM, and the desired configuration changes.

# Describe Azure Virtual Private Networks #

* A virtual private network (VPN) uses an encrypted tunnel within another network to connect two or more trusted private networks over an untrusted network (typically the public internet).
* Azure VPN Gateway instances are deployed in a dedicated subnet of the virtual network and enable the following connectivity options:
* Connect on-premises datacenters to virtual networks through a site-to-site connection.
* Connect individual devices to virtual networks through a point-to-site connection.
* Connect virtual networks to other virtual networks through a network-to-network connection.
* You can deploy only one VPN gateway in each virtual network, but one gateway can connect to multiple locations.
* There are two types of VPN gateways in Azure: policy-based and route-based.
* Policy-based VPN gateways specify statically the IP address of packets that should be encrypted through each tunnel, while route-based gateways use IP routing to decide which tunnel to use for each packet.
* Route-based VPNs are preferred for on-premises devices and are more resilient to topology changes.
* You can maximize the resiliency of your VPN gateway by using an active/standby configuration, active/active configuration, ExpressRoute failover, and zone-redundant gateways.
* In regions that support availability zones, VPN gateways and ExpressRoute gateways can be deployed in a zone-redundant configuration for resiliency, scalability, and higher availability.

# Describe Azure ExpressRoute #

* Azure ExpressRoute allows for private connections between on-premises networks and Microsoft cloud services like Azure and Office 365
* Connections are established through a connectivity provider and are called ExpressRoute circuits
* ExpressRoute connections offer higher reliability, faster speeds, consistent latencies, and higher security than typical internet connections
* Features and benefits include:
* Connectivity to Microsoft cloud services across all regions
* Global connectivity to Microsoft services through ExpressRoute Global Reach
* Dynamic routing between on-premises networks and Azure via BGP
* Built-in redundancy in every peering location for higher reliability
* ExpressRoute supports four connectivity models: CloudExchange colocation, point-to-point Ethernet connection, any-to-any connection, and Directly from ExpressRoute sites
* Security considerations include that data doesn't travel over the public internet and is not exposed to potential risks associated with internet communications.

# Describe Azure DNS #

* Azure DNS is a hosting service for DNS domains that uses Microsoft Azure infrastructure for name resolution
* Benefits of Azure DNS include: reliability and performance, security, ease of use, customizable virtual networks, and alias records
* Reliability and performance is achieved through Azure's global network of DNS name servers and anycast networking
* Security features include Azure RBAC, activity logs, and resource locking
* Azure DNS is integrated with the Azure portal and can be managed using Azure PowerShell cmdlets, Azure CLI, and REST API
* Supports private DNS domains, allowing the use of custom domain names in private virtual networks
* Alias record sets allow for seamless updates of IP addresses for underlying resources, such as Azure public IPs, Traffic Manager profiles, and CDN endpoints
* Azure DNS cannot be used to purchase domain names, but purchased domains can be hosted for record management in Azure DNS.

# Knowledge Check #

1. Which Azure Virtual Machine feature staggers updates across VMs based on their update domain and fault domain?
>Availability sets stagger VM updates based on their update and fault domains.

2. Which Azure service allows users to use a cloud hosted version of Windows from any location and connect from most modern browsers?
>Azure Virtual Desktop provides access to a cloud-hosted version of Windows, and it works with most modern browsers.
